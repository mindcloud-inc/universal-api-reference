# Rakuten Advertising: List advertisers

Retrieves advertisers from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-advertisers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-advertisers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-advertisers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        "string"
      ],
      "description": "string",
      "id": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "network": "string",
      "policies": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<string> |  |
| `description` | string |  |
| `id` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `network` | string |  |
| `policies` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /v2/advertisers` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-advertisers.md) for the provider-specific parameters and requirements.

