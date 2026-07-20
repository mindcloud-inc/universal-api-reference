# Clever Elements Universal API Examples

These examples use the MindCloud API key and Clever Elements connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/list-lists?${params}`, {
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
      "SOAP-ENV:Envelope": {}
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cleverElements/latest/actions/list-lists).

## Add List



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/add-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/add-list', {
  method: 'POST',
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
  "data": [
    {
      "SOAP-ENV:Envelope": {}
    }
  ],
  "meta": {}
}
```

See the full [Add List action reference](actions/add-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cleverElements/latest/actions/add-list).
