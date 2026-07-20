# OfficeClip: List Workflow Summaries

Retrieves workflow summaries from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-workflow-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-workflow-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0&entityType=string&entityId=string&stageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "entityType": "string",
  "entityId": "string",
  "stageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-workflow-summaries?${params}`, {
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
| `entityType` | string | yes | Required OfficeClip workflow entity type token. |
| `entityId` | string | yes | Required OfficeClip workflow entity serial id. |
| `stageId` | number | yes | Required OfficeClip workflow stage id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approveToUserId": {},
      "entityId": "string",
      "entityType": "string",
      "password": {},
      "rejectToUserId": {},
      "stageId": 1,
      "submitToUserId": {},
      "workflowType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approveToUserId` | object |  |
| `entityId` | string |  |
| `entityType` | string |  |
| `password` | object |  |
| `rejectToUserId` | object |  |
| `stageId` | number |  |
| `submitToUserId` | object |  |
| `workflowType` | string |  |

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/workflow-summary` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflow-summaries.md) for the provider-specific parameters and requirements.

