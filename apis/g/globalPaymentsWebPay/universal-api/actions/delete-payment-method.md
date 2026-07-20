# Global Payments WebPay: Delete Payment Method

Deletes a payment method from Global Payments WebPay.

```
DELETE https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/delete-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/delete-payment-method?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/delete-payment-method?${params}`, {
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
| `id` | string | yes | Global Payments payment method ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": {
        "id": "string",
        "result_code": "string",
        "time_created": "string",
        "type": "string"
      },
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action.id` | string |  |
| `action.result_code` | string |  |
| `action.time_created` | string |  |
| `action.type` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `DELETE /payment-methods/{id}` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-payment-method.md) for the provider-specific parameters and requirements.

