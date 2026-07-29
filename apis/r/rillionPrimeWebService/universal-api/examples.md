# Rillion Prime Web Service Universal API Examples

These examples use the MindCloud API key and Rillion Prime Web Service connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Account Coded Invoices

Count how many times an invoice has been account coded.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/count-account-coded-invoices?connectionId=$CONNECTION_ID&invoiceSeries=string&invoiceNo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "invoiceSeries": "string",
  "invoiceNo": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/count-account-coded-invoices?${params}`, {
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
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Count Account Coded Invoices action reference](actions/count-account-coded-invoices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rillionPrimeWebService/latest/actions/count-account-coded-invoices).

## Insert Account

Insert a general ledger account into the Prime register queue.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": {},
  "account.account": "string",
  "account.keyType": 1,
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": {},
    "account.account": "string",
    "account.keyType": 1,
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Insert Account action reference](actions/insert-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rillionPrimeWebService/latest/actions/insert-account).
