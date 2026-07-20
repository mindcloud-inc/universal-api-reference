# Maildrip: Verify a Paystack transaction



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-a-paystack-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-a-paystack-transaction?connectionId=$CONNECTION_ID&txref=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "txref": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/verify-a-paystack-transaction?${params}`, {
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
| `txref` | string | yes | The transaction reference. |
| `savecard` | string | no | Flag indicating whether to save the card or not. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "transaction": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `transaction` | object |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/payment/paystack/transactions/verify` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-a-paystack-transaction.md) for the provider-specific parameters and requirements.

