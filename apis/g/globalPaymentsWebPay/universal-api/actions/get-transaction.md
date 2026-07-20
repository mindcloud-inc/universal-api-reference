# Global Payments WebPay: Get Transaction

Retrieves a transaction from Global Payments WebPay.

```
GET https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-transaction?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/get-transaction?${params}`, {
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
| `id` | string | yes | Global Payments transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "amount": "string",
      "currency": "string",
      "id": "string",
      "merchant_id": "string",
      "status": "string",
      "time_created": "string",
      "time_last_updated": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string |  |
| `amount` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `merchant_id` | string |  |
| `status` | string |  |
| `time_created` | string |  |
| `time_last_updated` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `GET /transactions/{id}` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

