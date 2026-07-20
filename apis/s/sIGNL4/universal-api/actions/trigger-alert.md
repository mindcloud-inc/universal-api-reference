# SIGNL4: Trigger Alert

Creates an alert in SIGNL4.

```
POST https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/trigger-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/trigger-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "text": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/trigger-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "text": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes |  |
| `text` | string | yes |  |
| `title` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachments[]` | array<object> | no |  |
| `category` | string | no |  |
| `externalId` | string | no |  |
| `flags` | number | no | <p/><ul><li>0 = None</li><li>1 = HasAttachments</li><li>2 = HasAnnotations</li><li>4 = IsBreached</li><li>8 = HasLocationInfo</li><li>16 = EscalatedToTeam</li><li>32 = EscalatedToManager</li><li>64 = CreatedByEscalation</li></ul> |
| `parameters[]` | array<object> | no |  |
| `severity` | number | no | <p/><ul><li>0 = Low</li><li>1 = Major</li><li>2 = Critical</li></ul> |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alertingPatternId": "string",
      "alertingPatternName": "Ava Chen",
      "attachments": {
        "contentType": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "categoryId": "string",
      "categoryName": "Ava Chen",
      "escalations": [
        {}
      ],
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
      "parameters": {
        "id": "string",
        "name": "Ava Chen",
        "options": 1,
        "order": 1,
        "type": 1,
        "value": "string"
      },
      "requiredAcknowledgements": 1,
      "severity": 1,
      "status": {},
      "subscriptionId": "string",
      "teamId": "string",
      "text": "string",
      "timelineEntries": {
        "annotationtype": 1,
        "creatorId": "string",
        "creatorType": 1,
        "entrytype": 1,
        "id": "string",
        "order": 1,
        "remoteActionId": "string",
        "remoteJobId": "string",
        "teamId": "string",
        "text": "string",
        "timestamp": "2026-05-07T12:00:00.000Z",
        "userId": "string"
      },
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
| `attachments` | array<object> |  |
| `attachments.contentType` | string |  |
| `attachments.id` | string |  |
| `attachments.name` | string |  |
| `categoryId` | string |  |
| `categoryName` | string |  |
| `escalations` | array<object> |  |
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
| `parameters` | array<object> |  |
| `parameters.id` | string |  |
| `parameters.name` | string |  |
| `parameters.options` | number |  |
| `parameters.order` | number |  |
| `parameters.type` | number |  |
| `parameters.value` | string |  |
| `requiredAcknowledgements` | number |  |
| `severity` | number |  |
| `status` | object |  |
| `subscriptionId` | string |  |
| `teamId` | string |  |
| `text` | string |  |
| `timelineEntries` | array<object> |  |
| `timelineEntries.annotationtype` | number |  |
| `timelineEntries.creatorId` | string |  |
| `timelineEntries.creatorType` | number |  |
| `timelineEntries.entrytype` | number |  |
| `timelineEntries.id` | string |  |
| `timelineEntries.order` | number |  |
| `timelineEntries.remoteActionId` | string |  |
| `timelineEntries.remoteJobId` | string |  |
| `timelineEntries.teamId` | string |  |
| `timelineEntries.text` | string |  |
| `timelineEntries.timestamp` | date |  |
| `timelineEntries.userId` | string |  |
| `title` | string |  |
| `workflowType` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `POST /v2/alerts` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-alert.md) for the provider-specific parameters and requirements.

