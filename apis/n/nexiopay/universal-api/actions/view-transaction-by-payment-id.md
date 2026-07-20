# Nexiopay: View transaction by payment ID



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-transaction-by-payment-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-transaction-by-payment-id?connectionId=$CONNECTION_ID&paymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-transaction-by-payment-id?${params}`, {
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
| `paymentId` | string | yes | Nexio payment ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "paymentId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Transaction amount. |
| `currency` | string | Transaction currency. |
| `dateCreated` | date | Transaction creation timestamp. |
| `id` | string | Transaction ID. |
| `paymentId` | string | Nexio payment ID. |
| `status` | string | Transaction status. |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /transaction/v3/paymentId/{paymentId}` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-transaction-by-payment-id.md) for the provider-specific parameters and requirements.

