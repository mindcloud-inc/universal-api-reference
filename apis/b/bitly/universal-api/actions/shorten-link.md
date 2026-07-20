# Bitly: Shorten Link

Creates a shortened link in Bitly.

```
POST https://connect.mindcloud.co/v1/universal/bitly/latest/actions/shorten-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/shorten-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "longUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitly/latest/actions/shorten-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "longUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | The Bitly or branded short domain to use. |
| `forceNewLink` | boolean | no | Create a new link even if the long URL was shortened before. |
| `groupGuid` | string | no | The group GUID that should own the new bitlink. |
| `longUrl` | string | yes | The destination URL to shorten. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "string",
      "id": "string",
      "link": "https://example.com",
      "longUrl": "https://example.com",
      "references": {
        "group": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `id` | string |  |
| `link` | string |  |
| `longUrl` | string |  |
| `references.group` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `POST /shorten` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shorten-link.md) for the provider-specific parameters and requirements.

