# Erase.bg: Delete Folder

Deletes a folder from Erase.bg storage.

```
DELETE https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-folder?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/delete-folder?${params}`, {
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
| `id` | string | yes | Folder _id to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "path": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `path` | string |  |

## Native endpoint

Through the native Erase.bg API, this operation is `DELETE /service/platform/assets/v1.0/folders/:_id` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-folder.md) for the provider-specific parameters and requirements.

