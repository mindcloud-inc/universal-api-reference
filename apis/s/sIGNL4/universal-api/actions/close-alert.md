# SIGNL4: Close Alert

Updates an alert as closed in SIGNL4.

```
PUT https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/close-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/close-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alertId": "string",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/close-alert', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alertId": "string",
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alertId` | string | yes | Id to acknowledge an alert. |
| `uid` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `descr` | string | no |  |

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

Through the native SIGNL4 API, this operation is `POST /v2/alerts/{alertId}/close` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/close-alert.md) for the provider-specific parameters and requirements.

