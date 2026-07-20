# LimoExpress: List Currencies

Retrieves organization currencies from the LimoExpress platform.

```
GET https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-currencies?${params}`, {
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
      "active": 1,
      "code": "string",
      "id": "string",
      "name": "Ava Chen",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Currency active flag. |
| `code` | string | Currency code. |
| `id` | string | Currency identifier. |
| `name` | string | Currency name. |
| `symbol` | string | Currency symbol. |

## Native endpoint

Through the native LimoExpress API, this operation is `GET /api/integration/currencies` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-currencies.md) for the provider-specific parameters and requirements.

