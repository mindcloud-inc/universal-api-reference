# SIGNL4: Get Alert Details

Retrieves alert details from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-details?connectionId=$CONNECTION_ID&alertId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alertId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-details?${params}`, {
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
| `alertId` | string | yes | Alert you want to get. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no | User ID of user in which behave the api is called. It is used for filtering purposes regarding the alert. |

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

Through the native SIGNL4 API, this operation is `GET /v2/alerts/{alertId}/details` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert-details.md) for the provider-specific parameters and requirements.

