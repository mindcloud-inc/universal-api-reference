# Omnisend Universal API Examples

These examples use the MindCloud API key and Omnisend connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from Omnisend.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/list-contacts?${params}`, {
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

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/omnisend/latest/actions/list-contacts).

## Create Batch

Creates a batch request in Omnisend.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/create-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpoint": "string",
  "items[]": [
    {}
  ],
  "method": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/create-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpoint": "string",
    "items[]": [{}],
    "method": "string"
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

See the full [Create Batch action reference](actions/create-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/omnisend/latest/actions/create-batch).
