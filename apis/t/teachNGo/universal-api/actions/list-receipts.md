# Teach 'n Go: List Receipts

Retrieves receipts from Teach 'n Go.

```
GET https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-receipts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teach 'n Go `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-receipts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachNGo/latest/actions/list-receipts?${params}`, {
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
| `fromDate` | date | no | Only return receipts issued on or after this date. |
| `toDate` | date | no | Only return receipts issued on or before this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingDetails": "string",
      "billingName": "Ava Chen",
      "creditUseAmount": "string",
      "currencyCode": "string",
      "dateIssued": "2026-05-07T12:00:00.000Z",
      "discount": "string",
      "id": 1,
      "notes": "string",
      "paidBy": "string",
      "paymentDetails": [
        {
          "discount": "string",
          "paymentDescription": "string",
          "quantity": 1,
          "studentName": "Ava Chen",
          "subtotal": "string",
          "total": "string"
        }
      ],
      "receiptNo": "string",
      "subtotal": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingDetails` | string |  |
| `billingName` | string |  |
| `creditUseAmount` | string |  |
| `currencyCode` | string |  |
| `dateIssued` | date |  |
| `discount` | string |  |
| `id` | number |  |
| `notes` | string |  |
| `paidBy` | string |  |
| `paymentDetails[].discount` | string |  |
| `paymentDetails[].paymentDescription` | string |  |
| `paymentDetails[].quantity` | number |  |
| `paymentDetails[].studentName` | string |  |
| `paymentDetails[].subtotal` | string |  |
| `paymentDetails[].total` | string |  |
| `receiptNo` | string |  |
| `subtotal` | string |  |
| `total` | string |  |

## Native endpoint

Through the native Teach 'n Go API, this operation is `POST /api/v1/receipts` (base URL `https://app.teachngo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-receipts.md) for the provider-specific parameters and requirements.

