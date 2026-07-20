# Yampi: List Checkout Config

Retrieves the checkout configuration from Yampi.

```
GET https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-checkout-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yampi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-checkout-config?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yampi/latest/actions/list-checkout-config?${params}`, {
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
      "enabled": true,
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Yampi API, this operation is `GET /:merchantAlias/config/checkout` (base URL `https://api.dooki.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-checkout-config.md) for the provider-specific parameters and requirements.

