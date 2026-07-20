# Ruly Universal API Examples

These examples use the MindCloud API key and Ruly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Employees



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ruly/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ruly/latest/actions/list-employees?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Employees action reference](actions/list-employees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ruly/latest/actions/list-employees).

## Create Employee Record



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ruly/latest/actions/create-employee-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ruly/latest/actions/create-employee-record', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Employee Record action reference](actions/create-employee-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ruly/latest/actions/create-employee-record).
