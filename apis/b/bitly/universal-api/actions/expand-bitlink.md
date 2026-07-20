# Bitly: Expand Bitlink

Retrieves the long URL for a Bitly bitlink.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/expand-bitlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/expand-bitlink?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/expand-bitlink?${params}`, {
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
| `bitlinkId` | string | no | The Bitly bitlink ID to expand. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "link": "https://example.com",
      "longUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `link` | string |  |
| `longUrl` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `POST /expand` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/expand-bitlink.md) for the provider-specific parameters and requirements.

