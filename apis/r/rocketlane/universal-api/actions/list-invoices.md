# Rocketlane: List Invoices

Lists invoices in Rocketlane.

```
GET https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/list-invoices?${params}`, {
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
| `includeFields` | list<string> | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `match` | string | no | You can use the match param to specify if we need to filter the entries using either AND(all) / OR(any). Defaults to AND. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountOutstanding": 1,
      "amountPaid": 1,
      "amountWrittenOff": 1,
      "attachments": [
        {}
      ],
      "company": {},
      "createdAt": 1,
      "createdBy": {},
      "currency": "string",
      "dateOfIssue": "string",
      "dueDate": "string",
      "fields": [
        {}
      ],
      "invoiceId": 1,
      "invoiceNumber": "string",
      "notes": "string",
      "projects": [
        {}
      ],
      "status": "string",
      "subTotal": 1,
      "tax": 1,
      "updatedAt": 1,
      "updatedBy": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Total amount of the invoice including tax |
| `amountOutstanding` | number | Balance amount remaining to be paid |
| `amountPaid` | number | Total amount paid for this invoice |
| `amountWrittenOff` | number | Total amount written off for this invoice |
| `attachments` | array<object> | List of attachments associated with the invoice |
| `company` | object | Company details for the invoice |
| `createdAt` | number | Timestamp when the invoice was created |
| `createdBy` | object | The team member who last updated the invoice |
| `currency` | string | Currency of the invoice amount |
| `dateOfIssue` | string | Date when the invoice was issued. The format for the issue date is _YYYY-MM-DD_ |
| `dueDate` | string | Due date for the invoice payment. The format for the due date is _YYYY-MM-DD_ |
| `fields` | array<object> | Fields lists the custom invoice fields whose values were provided during invoice creation or updated later. Refer these [examples](https://developer.rocketlane.com/v1.0/docs/custom-fields#examples-of-requests-and-responses-for-assigning-custom-field-values) to know more about different types of custom fields returned in response. |
| `invoiceId` | number | Unique identifier of the invoice |
| `invoiceNumber` | string | Invoice number assigned to this invoice |
| `notes` | string | Notes or additional information about the invoice |
| `projects` | array<object> | List of projects mapped to this invoice |
| `status` | string | Current status of the invoice |
| `subTotal` | number | Total amount of the invoice excluding tax |
| `tax` | number | Tax amount applied to the invoice |
| `updatedAt` | number | Timestamp when the invoice was last updated |
| `updatedBy` | object | The team member who last updated the invoice |

## Native endpoint

Through the native Rocketlane API, this operation is `GET /1.0/invoices` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

