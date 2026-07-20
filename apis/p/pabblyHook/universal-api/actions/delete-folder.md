# Pabbly Hook: Delete Folder



```
DELETE https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/delete-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/delete-folder?connectionId=$CONNECTION_ID&folderId=664ef8fd7db74e5fd61ae0ad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "664ef8fd7db74e5fd61ae0ad"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/delete-folder?${params}`, {
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
| `folderId` | string | yes | Folder ID to delete. Example: `664ef8fd7db74e5fd61ae0ad`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Pabbly Hook folder deletion confirmation message. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `DELETE /api/v1/folders/:folderId` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-folder.md) for the provider-specific parameters and requirements.

