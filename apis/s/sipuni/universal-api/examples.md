# Sipuni Universal API Examples

These examples use the MindCloud API key and Sipuni connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Operators

Retrieves operators and presence statuses from Sipuni.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/list-operators?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/list-operators?${params}`, {
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

See the full [List Operators action reference](actions/list-operators.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sipuni/latest/actions/list-operators).

## Call Number



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/call-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string",
  "sipnumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/call-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string",
    "sipnumber": "string"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Call Number action reference](actions/call-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sipuni/latest/actions/call-number).
