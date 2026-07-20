# Webshipper: Create Return Shipping Method

Creates a return shipping method in Webshipper.

```
POST https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-shipping-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-shipping-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.name": "Ava Chen",
  "data.relationships.portal.data.id": "string",
  "data.relationships.shippingRate.data.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/create-return-shipping-method', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.name": "Ava Chen",
    "data.relationships.portal.data.id": "string",
    "data.relationships.shippingRate.data.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.attributes.name` | string | yes | Name of the return shipping method. |
| `data.relationships.portal.data.id` | string | yes | Return portal ID. |
| `data.relationships.shippingRate.data.id` | string | yes | Shipping rate ID. |

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

Through the native Webshipper API, this operation is `POST /return_shipping_methods` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-return-shipping-method.md) for the provider-specific parameters and requirements.

