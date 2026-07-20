# Zoho Books: List Customer Payments



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-customer-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-customer-payments?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-customer-payments?${params}`, {
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
| `amount` | number | no | Search payments by amount. |
| `customerId` | string | no | Customer ID for the payment. |
| `customerName` | string | no | Search payments by customer name. |
| `date` | string | no | Search payments by date. |
| `filterBy` | string | no | Filter payments by mode. |
| `notes` | string | no | Search payments by notes. |
| `organizationId` | string | yes | ID of the organization. |
| `paymentMode` | string | no | Search payments by payment mode. |
| `referenceNumber` | string | no | Search payments by reference number. |
| `searchText` | string | no | Search by reference number, customer name, or description. |
| `sortColumn` | string | no | Sort payments by the selected column. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "customerpayments": [
        {
          "accountId": "string",
          "accountName": "Ava Chen",
          "amount": 1,
          "bcyAmount": 1,
          "bcyRefundedAmount": 1,
          "bcyUnusedAmount": 1,
          "createdTime": "2026-05-07T12:00:00.000Z",
          "customerId": "string",
          "customerName": "Ava Chen",
          "date": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "hasAttachment": true,
          "invoiceNumbers": "string",
          "lastFourDigits": "string",
          "lastModifiedTime": "2026-05-07T12:00:00.000Z",
          "paymentGateway": "string",
          "paymentId": "string",
          "paymentMode": "string",
          "paymentModeFormatted": "string",
          "paymentNumber": "string",
          "paymentStatus": "string",
          "paymentType": "string",
          "referenceNumber": "string",
          "settlementStatus": "string",
          "taxAccountId": "string",
          "taxAccountName": "Ava Chen",
          "taxAmountWithheld": 1,
          "unusedAmount": 1
        }
      ],
      "message": "string",
      "pageContext": {
        "appliedFilter": "string",
        "hasMorePage": true,
        "page": 1,
        "perPage": 1,
        "reportName": "Ava Chen",
        "sortColumn": "string",
        "sortOrder": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `customerpayments[].accountId` | string |  |
| `customerpayments[].accountName` | string |  |
| `customerpayments[].amount` | number |  |
| `customerpayments[].bcyAmount` | number |  |
| `customerpayments[].bcyRefundedAmount` | number |  |
| `customerpayments[].bcyUnusedAmount` | number |  |
| `customerpayments[].createdTime` | date |  |
| `customerpayments[].customerId` | string |  |
| `customerpayments[].customerName` | string |  |
| `customerpayments[].date` | date |  |
| `customerpayments[].description` | string |  |
| `customerpayments[].hasAttachment` | boolean |  |
| `customerpayments[].invoiceNumbers` | string |  |
| `customerpayments[].lastFourDigits` | string |  |
| `customerpayments[].lastModifiedTime` | date |  |
| `customerpayments[].paymentGateway` | string |  |
| `customerpayments[].paymentId` | string |  |
| `customerpayments[].paymentMode` | string |  |
| `customerpayments[].paymentModeFormatted` | string |  |
| `customerpayments[].paymentNumber` | string |  |
| `customerpayments[].paymentStatus` | string |  |
| `customerpayments[].paymentType` | string |  |
| `customerpayments[].referenceNumber` | string |  |
| `customerpayments[].settlementStatus` | string |  |
| `customerpayments[].taxAccountId` | string |  |
| `customerpayments[].taxAccountName` | string |  |
| `customerpayments[].taxAmountWithheld` | number |  |
| `customerpayments[].unusedAmount` | number |  |
| `message` | string |  |
| `pageContext.appliedFilter` | string |  |
| `pageContext.hasMorePage` | boolean |  |
| `pageContext.page` | number |  |
| `pageContext.perPage` | number |  |
| `pageContext.reportName` | string |  |
| `pageContext.sortColumn` | string |  |
| `pageContext.sortOrder` | string |  |

## Native endpoint

Through the native Zoho Books API, this operation is `GET /customerpayments` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-payments.md) for the provider-specific parameters and requirements.

