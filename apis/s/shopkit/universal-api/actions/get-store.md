# Shopkit: Get Store

Retrieves store details from Shopkit.

```
GET https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopkit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-store?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopkit/latest/actions/get-store?${params}`, {
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
      "currency": "string",
      "description": "string",
      "email": "ava@example.com",
      "enable_shipping_methods": true,
      "name": "Ava Chen",
      "navigation": {},
      "settings": {},
      "show_email": true,
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `description` | string |  |
| `email` | string |  |
| `enable_shipping_methods` | boolean |  |
| `name` | string |  |
| `navigation` | object |  |
| `settings` | object |  |
| `show_email` | boolean |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Shopkit API, this operation is `GET /store` (base URL `https://api.shopk.it/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-store.md) for the provider-specific parameters and requirements.

