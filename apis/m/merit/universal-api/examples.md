# Merit Universal API Examples

These examples use the MindCloud API key and Merit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Taxes



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-taxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-taxes?${params}`, {
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
      "code": "string",
      "countryCode": {},
      "countryId": 1,
      "id": "string",
      "name": "Ava Chen",
      "nameEN": "Ava Chen",
      "nameRU": "Ava Chen",
      "nonActive": true,
      "taxPct": 1
    }
  ],
  "meta": {}
}
```

See the full [List Taxes action reference](actions/list-taxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/merit/latest/actions/list-taxes).

## Create Credit Invoice



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-credit-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Customer": {},
  "DocDate": "string",
  "DueDate": "string",
  "InvoiceNo": "string",
  "InvoiceRow[]": [
    {}
  ],
  "TaxAmount[]": [
    {}
  ],
  "TotalAmount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-credit-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Customer": {},
    "DocDate": "string",
    "DueDate": "string",
    "InvoiceNo": "string",
    "InvoiceRow[]": [{}],
    "TaxAmount[]": [{}],
    "TotalAmount": 1
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
      "CustomerId": "string",
      "InvoiceId": "string",
      "InvoiceNo": "string",
      "NewCustomer": "string",
      "RefNo": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Credit Invoice action reference](actions/create-credit-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/merit/latest/actions/create-credit-invoice).
