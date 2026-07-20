# Flokzu Universal API Examples

These examples use the MindCloud API key and Flokzu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Echo



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/echo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/echo?${params}`, {
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
      "param_string": "string"
    }
  ],
  "meta": {}
}
```

See the full [Echo action reference](actions/echo.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flokzu/latest/actions/echo).

## Add Record



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/add-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/add-record', {
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
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Record action reference](actions/add-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flokzu/latest/actions/add-record).
