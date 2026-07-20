# Confluence: Get Task

Retrieves an existing task from Confluence.

```
GET https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-task?connectionId=$CONNECTION_ID&cloudId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-task?${params}`, {
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
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | string | yes | ID of the task. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": {},
      "body": {},
      "completedAt": {},
      "completedBy": {},
      "createdAt": "string",
      "createdBy": "string",
      "dueAt": {},
      "id": "string",
      "localId": "string",
      "pageId": "string",
      "spaceId": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | object |  |
| `body` | object |  |
| `completedAt` | object |  |
| `completedBy` | object |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `dueAt` | object |  |
| `id` | string |  |
| `localId` | string |  |
| `pageId` | string |  |
| `spaceId` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Confluence API, this operation is `GET /ex/confluence/:cloudId/wiki/api/v2/tasks/:id` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.

