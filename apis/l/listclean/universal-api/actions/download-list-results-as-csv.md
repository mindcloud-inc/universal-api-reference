# Listclean: Download List Results As CSV

Retrieves verification list results as a CSV file from Listclean.

```
GET https://connect.mindcloud.co/v1/universal/listclean/latest/actions/download-list-results-as-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/download-list-results-as-csv?connectionId=$CONNECTION_ID&list_id=1&type=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "1",
  "type": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/download-list-results-as-csv?${params}`, {
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
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Raw CSV file content returned by the download endpoint. |

## Native endpoint

Through the native Listclean API, this operation is `GET /downloads/:list_id/:type` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-list-results-as-csv.md) for the provider-specific parameters and requirements.

