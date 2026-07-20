# Prodigi: Update Order Recipient

Updates recipient details for a Prodigi order.

```
PUT https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/update-order-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prodigi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/update-order-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prodigiOrderId": "string",
  "name": "Mr. Jeff Testing",
  "email": "jeff.testing@example.com",
  "phoneNumber": "123456780",
  "address": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/update-order-recipient', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prodigiOrderId": "string",
    "name": "Mr. Jeff Testing",
    "email": "jeff.testing@example.com",
    "phoneNumber": "123456780",
    "address": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prodigiOrderId` | string | yes | Prodigi order ID to update. |
| `name` | string | yes | Updated recipient name. Example: `Mr. Jeff Testing`. |
| `email` | string | yes | Updated recipient email address. Example: `jeff.testing@example.com`. |
| `phoneNumber` | string | yes | Updated recipient phone number. Example: `123456780`. |
| `address` | object | yes | Updated recipient address object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charges": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "items": [
        {}
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "merchantReference": "string",
      "metadata": {},
      "recipient": {},
      "shipments": [
        {}
      ],
      "shippingMethod": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charges` | array<object> | Order charges. |
| `created` | date | Order creation timestamp. |
| `id` | string | Prodigi order ID. |
| `items` | array<object> | Order items. |
| `lastUpdated` | date | Order last updated timestamp. |
| `merchantReference` | string | Merchant order reference. |
| `metadata` | object | Merchant metadata. |
| `recipient` | object | Recipient details. |
| `shipments` | array<object> | Order shipments. |
| `shippingMethod` | string | Requested shipping method. |
| `status` | object | Order status details. |

## Native endpoint

Through the native Prodigi API, this operation is `POST /orders/[:prodigiOrderId]/actions/updateRecipient` (base URL `https://api.prodigi.com/v4.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order-recipient.md) for the provider-specific parameters and requirements.

