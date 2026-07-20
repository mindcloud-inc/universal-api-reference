# GoAffPro: Update Payment Request

Updates an affiliate payment request in GoAffPro.

```
PUT https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-payment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-payment-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/update-payment-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Payment request ID. |
| `status` | string | yes | New payment request status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Updated payment request ID. |
| `status` | string | Updated payment request status. |
| `success` | boolean | Whether the payment request update succeeded. |

## Native endpoint

Through the native GoAffPro API, this operation is `PATCH /admin/payments/requests/:id` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-request.md) for the provider-specific parameters and requirements.

