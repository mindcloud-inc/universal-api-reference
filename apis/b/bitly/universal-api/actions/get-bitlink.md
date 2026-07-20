# Bitly: Get Bitlink

Retrieves a bitlink from your Bitly account.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-bitlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-bitlink?connectionId=$CONNECTION_ID&bitlink=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bitlink": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-bitlink?${params}`, {
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
| `bitlink` | string | yes | The Bitly bitlink to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "clientId": "string",
      "createdAt": "string",
      "createdBy": "string",
      "id": "string",
      "link": "https://example.com",
      "longUrl": "https://example.com",
      "references": {
        "group": "string"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `clientId` | string |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `id` | string |  |
| `link` | string |  |
| `longUrl` | string |  |
| `references.group` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /bitlinks/:bitlink` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bitlink.md) for the provider-specific parameters and requirements.

