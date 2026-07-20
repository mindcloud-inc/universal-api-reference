# Voucherify: Create Publication

Creates a publication in Voucherify for eligible vouchers.

```
POST https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-publication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-publication" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "voucherId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/create-publication', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "voucherId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes |  |
| `voucherId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "createdAt": "string",
      "customer": {},
      "customerId": "string",
      "id": "string",
      "metadata": {},
      "object": "string",
      "result": "string",
      "sourceId": "string",
      "trackingId": "string",
      "voucher": {},
      "vouchersId": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `createdAt` | string |  |
| `customer` | object |  |
| `customerId` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `result` | string |  |
| `sourceId` | string |  |
| `trackingId` | string |  |
| `voucher` | object |  |
| `vouchersId` | array<string> |  |

## Native endpoint

Through the native Voucherify API, this operation is `POST /publications` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-publication.md) for the provider-specific parameters and requirements.

