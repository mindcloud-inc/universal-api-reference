# Koncile OCR: Delete Folder



```
DELETE https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-folder?connectionId=$CONNECTION_ID&folder_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folder_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-folder?${params}`, {
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
| `folder_id` | number | yes | The folder identifier to delete. |
| `override` | boolean | no | Force deletion when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder_id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder_id` | number | The deleted folder identifier. |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Koncile OCR API, this operation is `DELETE /delete_folder` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-folder.md) for the provider-specific parameters and requirements.

