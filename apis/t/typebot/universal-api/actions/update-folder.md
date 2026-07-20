# Typebot: Update Folder



```
PUT https://connect.mindcloud.co/v1/universal/typebot/latest/actions/update-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/update-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typebot/latest/actions/update-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Folder ID to update. |
| `workspaceId` | string | yes | Workspace ID that owns the folder. |
| `folder.name` | string | no | Updated folder name. |
| `folder.parentFolderId` | string | no | Updated parent folder ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "parentFolderId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `parentFolderId` | string |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Typebot API, this operation is `PATCH /v1/folders/:folderId` (base URL `https://app.typebot.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-folder.md) for the provider-specific parameters and requirements.

