# Listclean: Get List Information

Retrieves verification list details from Listclean.

```
GET https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-list-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-list-information?connectionId=$CONNECTION_ID&list_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-list-information?${params}`, {
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
| `list_id` | number | yes | List ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_download": 1,
      "analytics": {},
      "cost": {},
      "filename": "Ava Chen",
      "list_id": 1,
      "request_time": "string",
      "size_for_human": "string",
      "size_in_bytes": 1,
      "status": "string",
      "upload_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_download` | number | Whether downloads are available. |
| `analytics` | object | Verification analytics summary. |
| `cost` | object | Cost summary. |
| `filename` | string | List filename. |
| `list_id` | number | Verification list ID. |
| `request_time` | string | List request timestamp. |
| `size_for_human` | string | Human-readable file size. |
| `size_in_bytes` | number | List file size in bytes. |
| `status` | string | List processing status. |
| `upload_id` | string | Provider upload ID. |

## Native endpoint

Through the native Listclean API, this operation is `GET /lists/:list_id` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-information.md) for the provider-specific parameters and requirements.

