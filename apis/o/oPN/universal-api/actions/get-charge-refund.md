# OPN: Get Charge Refund

Retrieves details for a charge refund from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-charge-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-charge-refund?connectionId=$CONNECTION_ID&id=string&refundId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "refundId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-charge-refund?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The charge ID that owns the refund. |
| `refundId` | string | yes | The refund ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acquirer_reference_number": "string",
      "amount": 1,
      "approval_code": "string",
      "capture": "string",
      "charge": "string",
      "created_at": "string",
      "currency": "string",
      "funding_amount": 1,
      "funding_currency": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "merchant_name": "Ava Chen",
      "merchant_uid": "string",
      "metadata": {},
      "object": "string",
      "status": "string",
      "terminal": "string",
      "voided": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acquirer_reference_number` | string |  |
| `amount` | number |  |
| `approval_code` | string |  |
| `capture` | string |  |
| `charge` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `funding_amount` | number |  |
| `funding_currency` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `merchant_name` | string |  |
| `merchant_uid` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `status` | string |  |
| `terminal` | string |  |
| `voided` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `GET /charges/:id/refunds/:refundId` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charge-refund.md) for the provider-specific parameters and requirements.

