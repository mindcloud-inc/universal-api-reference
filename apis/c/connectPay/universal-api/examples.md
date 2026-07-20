# ConnectPay Universal API Examples

These examples use the MindCloud API key and ConnectPay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Transactions

Retrieves bank account transactions from ConnectPay.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-account-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-account-transactions?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Account Transactions action reference](actions/get-account-transactions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/connectPay/latest/actions/get-account-transactions).

## Activate Card

Activates a ChipAndPin card in ConnectPay.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/activate-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/activate-card', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Activate Card action reference](actions/activate-card.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/connectPay/latest/actions/activate-card).
