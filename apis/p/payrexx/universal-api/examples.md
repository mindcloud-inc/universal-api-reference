# Payrexx Universal API Examples

These examples use the MindCloud API key and Payrexx connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Designs

Retrieves designs from Payrexx.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-designs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-designs?${params}`, {
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

See the full [List Designs action reference](actions/list-designs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payrexx/latest/actions/list-designs).

## Cancel Waiting Transaction

Cancels a waiting transaction in Payrexx.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/cancel-waiting-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/cancel-waiting-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123456"
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

See the full [Cancel Waiting Transaction action reference](actions/cancel-waiting-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payrexx/latest/actions/cancel-waiting-transaction).
