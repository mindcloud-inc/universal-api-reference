# Fintoc: List Payment Intents

Retrieves payment intents from Fintoc.

```
GET https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-payment-intents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-payment-intents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/list-payment-intents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "created_at": "string",
      "currency": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "recipient_account": {},
      "reference_id": "string",
      "sender_account": {},
      "status": "string",
      "transaction_date": "string",
      "widget_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `recipient_account` | object |  |
| `reference_id` | string |  |
| `sender_account` | object |  |
| `status` | string |  |
| `transaction_date` | string |  |
| `widget_token` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `GET /v1/payment_intents` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-intents.md) for the provider-specific parameters and requirements.

