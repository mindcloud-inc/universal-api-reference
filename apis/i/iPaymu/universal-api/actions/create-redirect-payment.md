# iPaymu: Create Redirect Payment

Create a payment session that redirects the buyer to the iPaymu payment page.

```
POST https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/create-redirect-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/create-redirect-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product[]": [
    "string"
  ],
  "qty[]": [
    1
  ],
  "price[]": [
    1
  ],
  "description[]": [
    "string"
  ],
  "notifyUrl": "https://example.com",
  "referenceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/create-redirect-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product[]": ["string"],
    "qty[]": [1],
    "price[]": [1],
    "description[]": ["string"],
    "notifyUrl": "https://example.com",
    "referenceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product[]` | array<string> | yes | Product name list. |
| `qty[]` | array<number> | yes | Product quantity list. |
| `price[]` | array<number> | yes | Product price list. |
| `description[]` | array<string> | yes | Product description list. |
| `notifyUrl` | string | yes | Callback URL for payment updates. |
| `referenceId` | string | yes | Merchant reference for the payment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sessionID": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sessionID` | string |  |
| `url` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `POST /payment` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-redirect-payment.md) for the provider-specific parameters and requirements.

