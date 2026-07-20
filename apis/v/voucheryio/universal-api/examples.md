# Vouchery.io Universal API Examples

These examples use the MindCloud API key and Vouchery.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User and Project



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-current-user-and-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-current-user-and-project?${params}`, {
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

See the full [Get Current User and Project action reference](actions/get-current-user-and-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voucheryio/latest/actions/get-current-user-and-project).

## Confirm Redemption By Transaction ID



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/confirm-redemption-by-transaction-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/confirm-redemption-by-transaction-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": "string"
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

See the full [Confirm Redemption By Transaction ID action reference](actions/confirm-redemption-by-transaction-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voucheryio/latest/actions/confirm-redemption-by-transaction-id).
