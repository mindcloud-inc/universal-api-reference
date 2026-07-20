# QuickFile: Get Payment



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-payment?connectionId=$CONNECTION_ID&paymentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-payment?${params}`, {
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
| `paymentId` | number | yes | The QuickFile PaymentID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "invoiceId": 1,
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentId": 1,
      "paymentMethod": "string",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Payment amount. |
| `invoiceId` | number | Linked invoice identifier. |
| `paymentDate` | date | Payment date. |
| `paymentId` | number | QuickFile payment identifier. |
| `paymentMethod` | string | Payment method name. |
| `reference` | string | Payment reference. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /payment/get` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment.md) for the provider-specific parameters and requirements.

