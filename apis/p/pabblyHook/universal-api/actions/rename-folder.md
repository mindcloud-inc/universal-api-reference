# Pabbly Hook: Rename Folder



```
PUT https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/rename-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/rename-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "664ef8fd7db74e5fd61ae0ad",
  "name": "Operations archive"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/rename-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "664ef8fd7db74e5fd61ae0ad",
    "name": "Operations archive"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Folder ID from Pabbly Hook. Example: `664ef8fd7db74e5fd61ae0ad`. |
| `name` | string | yes | New folder name. Example: `Operations archive`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | object | Renamed folder object. |
| `message` | string | Pabbly Hook folder rename confirmation message. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `PUT /api/v1/folders/rename/:folderId` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-folder.md) for the provider-specific parameters and requirements.

