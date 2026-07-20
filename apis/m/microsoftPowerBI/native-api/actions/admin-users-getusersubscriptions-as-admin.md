# Users GetUserSubscriptionsAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/users/[:userId]/subscriptions`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Users GetUserSubscriptionsAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/users-get-user-subscriptions-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The graph ID or user principal name (UPN) of the user |
| `continuationToken` | query | `string` | no | Token required to get the next chunk of the result set |
