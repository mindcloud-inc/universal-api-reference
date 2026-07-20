# Bitly: Update Bitlink

Updates an existing bitlink in Bitly.

```
PUT https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-bitlink
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-bitlink" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bitlink": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitly/latest/actions/update-bitlink', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bitlink": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bitlink` | string | yes |  |
| `title` | string | no |  |

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

Through the native Bitly API, this operation is `PATCH /bitlinks/:bitlink` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bitlink.md) for the provider-specific parameters and requirements.

