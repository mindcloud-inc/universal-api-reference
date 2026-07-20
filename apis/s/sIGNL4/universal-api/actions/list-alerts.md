# SIGNL4: List Alerts

Retrieves alerts from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-alerts?connectionId=$CONNECTION_ID&userId=sample-user-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "sample-user-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-alerts?${params}`, {
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
| `userId` | string | yes | User ID of the user to get alerts for. Required when using SIGNL4 API key authentication. Example: `sample-user-id`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | User ID of the user you want to get alerts for. |
| `maxResults` | number | no | Defines the limit of retrieved alert details per request. 1 to 100 are allowed per request. Number of alerts could be less if filtered but at least 1. Default: `100`. |
| `maxResults` | number | no | Maximum number of alerts to return. SIGNL4 allows 1 to 100. Default: `5`. Example: `5`. |
| `teamIds[]` | array<string> | no |  |
| `alertIds[]` | array<string> | no |  |
| `afterId` | string | no |  |
| `categoryIds[]` | array<string> | no |  |
| `continuationToken.nextPartitionKey` | string | no |  |
| `continuationToken.nextRowKey` | string | no |  |
| `continuationToken.nextTableName` | string | no |  |
| `maxCreated` | date | no |  |
| `minCreated` | date | no |  |
| `modifiedSince` | date | no |  |
| `showPersonalHiddenCategories` | boolean | no |  |
| `userCreatedAlertsFilterMode` | number | no | <p/><ul><li>0 = ExcludeUserCreatedAlerts</li><li>1 = IncludeUserCreatedAlerts</li><li>2 = OnlyUserCreatedAlerts</li></ul> |
| `alertStatusCodes` | number | no | <p/><ul><li>0 = None</li><li>1 = Open</li><li>2 = Acknowledged</li><li>4 = Closed</li><li>8 = NoReply</li><li>16 = Failed</li><li>32 = Error</li></ul> |
| `textToSearch` | string | no |  |
| `externalId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertingPatternId": "string",
      "alertingPatternName": "Ava Chen",
      "categoryId": "string",
      "categoryName": "Ava Chen",
      "eventDistributionId": "string",
      "eventDistributionName": "Ava Chen",
      "eventId": "string",
      "eventSourceId": "string",
      "externalId": "string",
      "flags": 1,
      "history": {
        "acknowledgedAt": "2026-05-07T12:00:00.000Z",
        "acknowledgements": [
          "string"
        ],
        "closedAt": "2026-05-07T12:00:00.000Z",
        "closedBy": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "createdBy": "string",
        "createdByName": "Ava Chen"
      },
      "id": "string",
      "lastModified": "2026-05-07T12:00:00.000Z",
      "requiredAcknowledgements": 1,
      "severity": 1,
      "status": {},
      "subscriptionId": "string",
      "teamId": "string",
      "text": "string",
      "title": "string",
      "workflowType": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertingPatternId` | string |  |
| `alertingPatternName` | string |  |
| `categoryId` | string |  |
| `categoryName` | string |  |
| `eventDistributionId` | string |  |
| `eventDistributionName` | string |  |
| `eventId` | string |  |
| `eventSourceId` | string |  |
| `externalId` | string |  |
| `flags` | number |  |
| `history` | object |  |
| `history.acknowledgedAt` | date |  |
| `history.acknowledgements` | array<string> |  |
| `history.closedAt` | date |  |
| `history.closedBy` | string |  |
| `history.created` | date |  |
| `history.createdBy` | string |  |
| `history.createdByName` | string |  |
| `id` | string |  |
| `lastModified` | date |  |
| `requiredAcknowledgements` | number |  |
| `severity` | number |  |
| `status` | object |  |
| `subscriptionId` | string |  |
| `teamId` | string |  |
| `text` | string |  |
| `title` | string |  |
| `workflowType` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `POST /v2/alerts/paged` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts.md) for the provider-specific parameters and requirements.

