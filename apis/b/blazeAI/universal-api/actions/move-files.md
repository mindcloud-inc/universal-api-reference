# Blaze AI: Move Files

Moves files between folders in Blaze AI.

```
PUT https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/move-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/move-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspace_id": "994619"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/move-files', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspace_id": "994619"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace_id` | number | yes | Default: `994619`. |
| `folderIds` | string | no | Default: `3421508`. |
| `docIds` | string | no |  |
| `destinationFolderId` | number | no | Default: `3413829`. |
| `destinationWorkspaceId` | number | no | Default: `994619`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Blaze AI API, this operation is `POST /api/v1/w/:workspace_id/files/move` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-files.md) for the provider-specific parameters and requirements.

