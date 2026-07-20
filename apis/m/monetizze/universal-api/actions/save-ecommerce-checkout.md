# Monetizze: Save Ecommerce Checkout

Creates an ecommerce checkout in Monetizze.

```
POST https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/save-ecommerce-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/save-ecommerce-checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/save-ecommerce-checkout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes | Full Monetizze ecommerce checkout JSON object as documented for this endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "codigo_checkout": "string",
      "url_checkout": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `codigo_checkout` | string | Checkout hash returned by Monetizze for the saved order. |
| `url_checkout` | string | Checkout URL where the customer can complete payment. |

## Native endpoint

Through the native Monetizze API, this operation is `POST /ecommerce/checkout` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-ecommerce-checkout.md) for the provider-specific parameters and requirements.

