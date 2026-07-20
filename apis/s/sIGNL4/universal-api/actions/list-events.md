# SIGNL4: List Events

Retrieves events from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxResults` | number | no | Defines the limit of retrieved alert details per request. 1 to 100 are allowed per request. Number of alerts could be less if filtered but at least 1. |
| `maxResults` | number | no | Maximum number of events to return. SIGNL4 allows 1 to 100. Default: `5`. Example: `5`. |
| `teamid` | string | no |  |
| `continuationToken.nextPartitionKey` | string | no |  |
| `continuationToken.nextRowKey` | string | no |  |
| `continuationToken.nextTableName` | string | no |  |
| `eventStatusCode` | number | no | <p/><ul><li>0 = None</li><li>1 = Processing</li><li>2 = Signled</li><li>3 = Filtered</li><li>4 = Resolved</li><li>5 = Discarded</li><li>6 = Acknowledged</li><li>7 = Suppressed</li><li>8 = NoRuleApplied</li><li>9 = MultipleTargetStatus</li><li>21 = WaitingForAutoClose</li><li>22 = NotEnoughOccurrences</li><li>23 = DuplicateSuppressed</li><li>30 = NoTarget</li><li>1000 = Error</li></ul> |
| `maxCreationDate` | date | no |  |
| `minCreationDate` | date | no |  |
| `modifiedSince` | date | no |  |
| `textToSearch` | string | no |  |
| `eventSourceId` | string | no |  |
| `eventCreatorFilter.userId` | string | no |  |
| `eventCreatorFilter.userCreatedFilterMode` | number | no | <p/><ul><li>0 = ExcludeUserCreatedEvents</li><li>1 = IncludeUserCreatedEvents</li><li>2 = OnlyUserCreatedEvents</li></ul> |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledgedAlerts": [
        "string"
      ],
      "alertId": "string",
      "categoryId": "string",
      "closedAlerts": [
        "string"
      ],
      "createdByUserId": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "eventSourceGroupId": "string",
      "eventSourceId": "string",
      "eventSourceTeamId": "string",
      "eventSourceType": 1,
      "eventStatus": 1,
      "id": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "severity": 1,
      "teamId": "string",
      "text": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acknowledgedAlerts` | array<string> |  |
| `alertId` | string |  |
| `categoryId` | string |  |
| `closedAlerts` | array<string> |  |
| `createdByUserId` | string |  |
| `creationTime` | date |  |
| `eventSourceGroupId` | string |  |
| `eventSourceId` | string |  |
| `eventSourceTeamId` | string |  |
| `eventSourceType` | number |  |
| `eventStatus` | number |  |
| `id` | string |  |
| `lastModified` | date |  |
| `severity` | number |  |
| `teamId` | string |  |
| `text` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `POST /v2/events/paged` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

