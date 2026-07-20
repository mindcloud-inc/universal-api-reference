# condoo: Retrieve Account Payment

Retrieves an account payment from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-account-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-account-payment?connectionId=$CONNECTION_ID&paymentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-account-payment?${params}`, {
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
| `paymentId` | number | yes | Required payment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "frequency": "string",
      "id": 1,
      "name": "Ava Chen",
      "plan_id": 1,
      "processor": "string",
      "status": true,
      "total_amount": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `datetime` | date |  |
| `email` | string |  |
| `frequency` | string |  |
| `id` | number |  |
| `name` | string |  |
| `plan_id` | number |  |
| `processor` | string |  |
| `status` | boolean |  |
| `total_amount` | string |  |
| `type` | string |  |

## Native endpoint

Through the native condoo API, this operation is `GET /payments/{payment_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-account-payment.md) for the provider-specific parameters and requirements.

