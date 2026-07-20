# Listclean: Download List Results As JSON

Retrieves verification list results as JSON from Listclean.

```
GET https://connect.mindcloud.co/v1/universal/listclean/latest/actions/download-list-results-as-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/download-list-results-as-json?connectionId=$CONNECTION_ID&list_id=1&type=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "1",
  "type": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/download-list-results-as-json?${params}`, {
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
| `list_id` | number | yes | List ID whose results should be downloaded. |
| `type` | list | yes | Result type to download: clean, dirty, or unknown. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "remarks": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address in the downloaded result. |
| `remarks` | string | Provider remarks for the downloaded result. |
| `status` | string | Verification status in the downloaded result. |

## Native endpoint

Through the native Listclean API, this operation is `GET /downloads/json/:list_id/:type` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-list-results-as-json.md) for the provider-specific parameters and requirements.

