# Peggy Pay: Get Order by Submission Hash

Retrieves an order from Peggy Pay by submission hash.

```
GET https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/get-order-by-submission-hash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peggy Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/get-order-by-submission-hash?connectionId=$CONNECTION_ID&hash=abc123submissionhash" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "abc123submissionhash"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peggyPay/latest/actions/get-order-by-submission-hash?${params}`, {
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
| `hash` | string | yes | Submission hash (`peggyHash`) from a Peggy Pay redirect or webhook. Example: `abc123submissionhash`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Amount": 1,
      "AmountEx": 1,
      "AmountVat": 1,
      "Customer": {},
      "Description": "string",
      "Hash": "string",
      "InvoiceNumber": "string",
      "OrderLines": [
        {}
      ],
      "PaymentDate": "2026-05-07T12:00:00.000Z",
      "PaymentType": "string",
      "Status": "string",
      "VatAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Amount` | number | Order amount in minor units as returned by Peggy Pay. |
| `AmountEx` | number | Order amount excluding VAT. |
| `AmountVat` | number | Order VAT amount. |
| `Customer` | object | Customer details associated with the order. |
| `Description` | string | Order description. |
| `Hash` | string | Peggy Pay order hash. |
| `InvoiceNumber` | string | Invoice number associated with the order. |
| `OrderLines` | array<object> | Order line records. |
| `PaymentDate` | date | Payment date. |
| `PaymentType` | string | Order payment type. |
| `Status` | string | Order status. |
| `VatAmount` | number | VAT percentage or amount returned by Peggy Pay. |

## Native endpoint

Through the native Peggy Pay API, this operation is `GET Formbuilder.Submissions.getOrder` (base URL `https://www.peggypay.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-by-submission-hash.md) for the provider-specific parameters and requirements.

