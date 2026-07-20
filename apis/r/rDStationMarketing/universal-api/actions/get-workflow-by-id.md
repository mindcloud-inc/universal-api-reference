# RD Station Marketing: Get Workflow by ID



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-workflow-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-workflow-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/get-workflow-by-id?${params}`, {
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
| `id` | string | yes | Workflow ID in path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "workflowInfo": {
        "actions": [
          {
            "id": "string",
            "type": "string"
          }
        ],
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workflowInfo.actions[].id` | string |  |
| `workflowInfo.actions[].type` | string |  |
| `workflowInfo.createdAt` | date |  |
| `workflowInfo.id` | string |  |
| `workflowInfo.name` | string |  |
| `workflowInfo.status` | string |  |
| `workflowInfo.updatedAt` | date |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `GET /platform/workflows/:id` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-by-id.md) for the provider-specific parameters and requirements.

