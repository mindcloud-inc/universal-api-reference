# Global Payments WebPay: Get Settlement Deposit

Retrieves a settlement deposit from Global Payments WebPay.

```
GET https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-settlement-deposit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-settlement-deposit?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-settlement-deposit?${params}`, {
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
| `id` | string | yes | Global Payments settlement deposit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregation_model": "string",
      "amount": "string",
      "bank_transfer": {
        "masked_account_number_last4": "string"
      },
      "currency": "string",
      "funding_type": "string",
      "id": "string",
      "status": "string",
      "time_created": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregation_model` | string |  |
| `amount` | string |  |
| `bank_transfer.masked_account_number_last4` | string |  |
| `currency` | string |  |
| `funding_type` | string |  |
| `id` | string |  |
| `status` | string |  |
| `time_created` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `GET /settlement/deposits/{id}` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-settlement-deposit.md) for the provider-specific parameters and requirements.

