# List Alerts with SIGNL4

Retrieves alerts from SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/alerts/paged`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [List Alerts](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | query | `string` | no | User ID of the user you want to get alerts for. |
| `userId` | query | `string` | yes | User ID of the user to get alerts for. Required when using SIGNL4 API key authentication. |
| `maxResults` | query | `number` | no | Defines the limit of retrieved alert details per request. 1 to 100 are allowed per request. Number of alerts could be less if filtered but at least 1. |
| `maxResults` | query | `number` | no | Maximum number of alerts to return. SIGNL4 allows 1 to 100. |
| `teamIds[]` | body | `array<string>` | no | — |
| `alertIds[]` | body | `array<string>` | no | — |
| `afterId` | body | `string` | no | — |
| `categoryIds[]` | body | `array<string>` | no | — |
| `continuationToken.nextPartitionKey` | body | `string` | no | — |
| `continuationToken.nextRowKey` | body | `string` | no | — |
| `continuationToken.nextTableName` | body | `string` | no | — |
| `maxCreated` | body | `date` | no | — |
| `minCreated` | body | `date` | no | — |
| `modifiedSince` | body | `date` | no | — |
| `showPersonalHiddenCategories` | body | `boolean` | no | — |
| `userCreatedAlertsFilterMode` | body | `number` | no | <p/><ul><li>0 = ExcludeUserCreatedAlerts</li><li>1 = IncludeUserCreatedAlerts</li><li>2 = OnlyUserCreatedAlerts</li></ul> |
| `alertStatusCodes` | body | `number` | no | <p/><ul><li>0 = None</li><li>1 = Open</li><li>2 = Acknowledged</li><li>4 = Closed</li><li>8 = NoReply</li><li>16 = Failed</li><li>32 = Error</li></ul> |
| `textToSearch` | body | `string` | no | — |
| `externalId` | body | `string` | no | — |
