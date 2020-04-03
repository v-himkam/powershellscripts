- [Azure_APIManagement_AuthZ_Grant_Min_RBAC_Access](output.md#Azure_APIManagement_AuthZ_Grant_Min_RBAC_Access)

- [Azure_APIManagement_Audit_Enable_Alerts](output.md#Azure_APIManagement_Audit_Enable_Alerts)

## Azure_APIManagement_AuthZ_Grant_Min_RBAC_Access
|Description|Recommendation|Notes
|---------:|----------:|-------------:|
|All users/identities must be granted minimum required permissions using Role Based Access Control (RBAC)|Remove any excessive privileges granted on the API Management Service. Run command: Remove-AzRoleAssignment -SignInName '<SignInName>' -Scope '<Scope>' -RoleDefinitionName '<RoleDefinitionName>'. Run 'Get-Help Remove-AzRoleAssignment -full' for more help.|



## Azure_APIManagement_Audit_Enable_Alerts
|Description|Recommendation|Notes
|---------:|----------:|-------------:|
|Metric alert rules must be configured for critical actions on API Management service|To setup an alert rule: (1) Go to API management instance -> 'Alerts' -> 'New alert rule' -> 'Add condition' (2) Select Signal type as 'Metrics' -> Select 'Unauthorized Gateway Request' -> Select a. Operator = 'Greater Than' b. Aggregation type = 'Total' c. Threshold value = '0' and d. Aggregation granularity = '1 hour' (3) Select an existing Action Group or create a new one of type 'Email/SMS/Push/Voice'. Select 'Email' option and specify the email id. Please refer: https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-use-azure-monitor#set-up-an-alert-rule-for-unauthorized-request.|



