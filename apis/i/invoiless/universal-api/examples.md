# Invoiless Universal API Examples

These examples use the MindCloud API key and Invoiless connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Invoices

Retrieves invoices from Invoiless.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/list-invoices?${params}`, {
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
      "__v": 1,
      "_id": "string",
      "acceptPayment": true,
      "attachments": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": {
        "__v": 1,
        "_id": "string",
        "attachPdf": true,
        "billTo": {
          "company": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "shortName": "Ava Chen"
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "id": "string",
        "property": "string",
        "shipTo": {
          "company": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "shortName": "Ava Chen"
        }
      },
      "date": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isOverdue": true,
      "isRetainer": true,
      "items": [
        {
          "_id": "string",
          "id": "string",
          "name": "Ava Chen",
          "price": 1,
          "quantity": 1
        }
      ],
      "kind": "string",
      "lang": "string",
      "netTotal": 1,
      "notes": "string",
      "number": "string",
      "overdueAlertSent": true,
      "property": {
        "_id": "string",
        "id": "string"
      },
      "shipTo": true,
      "status": "string",
      "subTotal": 1,
      "tax": 1,
      "taxIncluded": true,
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Invoices action reference](actions/list-invoices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invoiless/latest/actions/list-invoices).

## Create Customer

Creates a new customer in Invoiless.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billTo": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billTo": {}
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
      "__v": 1,
      "_id": "string",
      "attachPdf": true,
      "billTo": {
        "company": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "isArchived": true,
      "notes": "string",
      "property": "string",
      "shipTo": {
        "company": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invoiless/latest/actions/create-customer).
