# Global Payments WebPay: Update Payer

Updates a payer in Global Payments WebPay.

```
PUT https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/update-payer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/update-payer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/update-payer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Global Payments payer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "merchant_id": "string",
      "reference": "string",
      "time_created": "2026-05-07T12:00:00.000Z",
      "time_last_updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `merchant_id` | string |  |
| `reference` | string |  |
| `time_created` | date |  |
| `time_last_updated` | date |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `PATCH /payers/{id}` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payer.md) for the provider-specific parameters and requirements.

