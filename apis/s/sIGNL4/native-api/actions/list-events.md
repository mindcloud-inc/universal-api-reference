# List Events with SIGNL4

Retrieves events from SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/events/paged`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [List Events](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `maxResults` | query | `number` | no | Defines the limit of retrieved alert details per request. 1 to 100 are allowed per request. Number of alerts could be less if filtered but at least 1. |
| `maxResults` | query | `number` | no | Maximum number of events to return. SIGNL4 allows 1 to 100. |
| `teamid` | body | `string` | no | — |
| `continuationToken.nextPartitionKey` | body | `string` | no | — |
| `continuationToken.nextRowKey` | body | `string` | no | — |
| `continuationToken.nextTableName` | body | `string` | no | — |
| `eventStatusCode` | body | `number` | no | <p/><ul><li>0 = None</li><li>1 = Processing</li><li>2 = Signled</li><li>3 = Filtered</li><li>4 = Resolved</li><li>5 = Discarded</li><li>6 = Acknowledged</li><li>7 = Suppressed</li><li>8 = NoRuleApplied</li><li>9 = MultipleTargetStatus</li><li>21 = WaitingForAutoClose</li><li>22 = NotEnoughOccurrences</li><li>23 = DuplicateSuppressed</li><li>30 = NoTarget</li><li>1000 = Error</li></ul> |
| `maxCreationDate` | body | `date` | no | — |
| `minCreationDate` | body | `date` | no | — |
| `modifiedSince` | body | `date` | no | — |
| `textToSearch` | body | `string` | no | — |
| `eventSourceId` | body | `string` | no | — |
| `eventCreatorFilter.userId` | body | `string` | no | — |
| `eventCreatorFilter.userCreatedFilterMode` | body | `number` | no | <p/><ul><li>0 = ExcludeUserCreatedEvents</li><li>1 = IncludeUserCreatedEvents</li><li>2 = OnlyUserCreatedEvents</li></ul> |
