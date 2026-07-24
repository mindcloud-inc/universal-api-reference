# Rillion Prime Pay: List Pending Supplier Payments



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-pending-supplier-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-pending-supplier-payments?connectionId=$CONNECTION_ID&supplierId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "supplierId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-pending-supplier-payments?${params}`, {
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
| `supplierId` | string | yes | Supplier ID to list pending payments for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paymentApprovedCount": 1,
      "paymentAwaitingApprovalCount": 1,
      "paymentCreatedCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paymentApprovedCount` | number |  |
| `paymentAwaitingApprovalCount` | number |  |
| `paymentCreatedCount` | number |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/supplier/payments/pending` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pending-supplier-payments.md) for the provider-specific parameters and requirements.

