# Finmei Universal API Examples

These examples use the MindCloud API key and Finmei connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Invoices



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "businessId": "string",
          "buyer": {
            "firstName": "Ava",
            "lastName": "Chen",
            "type": "string"
          },
          "createdAt": 1,
          "currency": "string",
          "id": "string",
          "invoiceDate": "string",
          "invoiceNumber": "string",
          "invoiceType": "string",
          "items": [
            {
              "name": "Ava Chen",
              "price": 1,
              "quantity": 1,
              "units": "string",
              "vatPercentage": 1
            }
          ],
          "paymentStatus": "string",
          "shareLink": "https://example.com",
          "totalInclVat": 1,
          "updatedAt": 1
        }
      ],
      "meta": {
        "currentPage": 1,
        "lastPage": 1,
        "path": "string",
        "perPage": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [List Invoices action reference](actions/list-invoices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finmei/latest/actions/list-invoices).

## Create Expense



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currency": "string",
  "date": "2026-05-07T12:00:00.000Z",
  "file": "string",
  "seller": "string",
  "total": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmei/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currency": "string",
    "date": "2026-05-07T12:00:00.000Z",
    "file": "string",
    "seller": "string",
    "total": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": 1,
        "currency": "string",
        "date": "string",
        "id": "string",
        "seller": "string",
        "total": 1,
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Expense action reference](actions/create-expense.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finmei/latest/actions/create-expense).
