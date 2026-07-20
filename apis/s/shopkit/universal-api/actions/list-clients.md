# Shopkit: List Clients

Retrieves clients from Shopkit.

```
GET https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/list-clients?${params}`, {
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
      "accepts_marketing": true,
      "billing": {},
      "company": "string",
      "created_at": 1,
      "delivery": {},
      "email": "ava@example.com",
      "hash": "string",
      "id": 1,
      "is_banned": true,
      "is_deleted": true,
      "is_registered": true,
      "last_seen_at": 1,
      "name": "Ava Chen",
      "type": "string",
      "wholesale": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepts_marketing` | boolean |  |
| `billing` | object |  |
| `company` | string |  |
| `created_at` | number |  |
| `delivery` | object |  |
| `email` | string |  |
| `hash` | string |  |
| `id` | number |  |
| `is_banned` | boolean |  |
| `is_deleted` | boolean |  |
| `is_registered` | boolean |  |
| `last_seen_at` | number |  |
| `name` | string |  |
| `type` | string |  |
| `wholesale` | boolean |  |

## Native endpoint

Through the native Shopkit API, this operation is `GET /client` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

