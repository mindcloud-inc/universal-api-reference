# Webshipper: List Return Shipping Methods

Retrieves return shipping methods from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-return-shipping-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-return-shipping-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-return-shipping-methods?${params}`, {
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
      "excluded_countries": [
        "string"
      ],
      "excluded_skus": [
        "string"
      ],
      "excluded_zip_codes": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `excluded_countries` | array<string> |  |
| `excluded_skus` | array<string> |  |
| `excluded_zip_codes` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /return_shipping_methods` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-return-shipping-methods.md) for the provider-specific parameters and requirements.

