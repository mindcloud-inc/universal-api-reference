# ClustDoc: List Uploads By Dossier Item



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-uploads-by-dossier-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-uploads-by-dossier-item?connectionId=$CONNECTION_ID&dossier_item_id=14568006" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dossier_item_id": "14568006"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-uploads-by-dossier-item?${params}`, {
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
| `dossier_item_id` | string | yes | Return uploads for a specific dossier item. Default: `14568006`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "dossier_id": 1,
      "dossier_item_id": 1,
      "id": 1,
      "mime_type": "string",
      "name": "Ava Chen",
      "size": 1,
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `dossier_id` | number |  |
| `dossier_item_id` | number |  |
| `id` | number |  |
| `mime_type` | string |  |
| `name` | string |  |
| `size` | number |  |
| `updated_at` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /uploads` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-uploads-by-dossier-item.md) for the provider-specific parameters and requirements.

