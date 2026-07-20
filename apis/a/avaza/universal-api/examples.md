# Avaza Universal API Examples

These examples use the MindCloud API key and Avaza connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves account details from Avaza.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/get-account-details?${params}`, {
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

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avaza/latest/actions/get-account-details).

## Create Bill

Creates a new bill in Avaza.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lineitems": {},
  "lineitems[].quantity": 1,
  "lineitems[].unitprice": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-bill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lineitems": {},
    "lineitems[].quantity": 1,
    "lineitems[].unitprice": 1
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

See the full [Create Bill action reference](actions/create-bill.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avaza/latest/actions/create-bill).
