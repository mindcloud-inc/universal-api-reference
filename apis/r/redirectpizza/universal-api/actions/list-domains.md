# redirect.pizza: List Domains



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/list-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/list-domains?${params}`, {
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
      "createdAt": "string",
      "dns": {},
      "fqdn": "string",
      "hsts": true,
      "id": 1,
      "isRootDomain": true,
      "preventForeignEmbedding": true,
      "referrerPolicy": "string",
      "ssl": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `dns` | object |  |
| `fqdn` | string |  |
| `hsts` | boolean |  |
| `id` | number |  |
| `isRootDomain` | boolean |  |
| `preventForeignEmbedding` | boolean |  |
| `referrerPolicy` | string |  |
| `ssl` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `GET /api/v1/domains` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

