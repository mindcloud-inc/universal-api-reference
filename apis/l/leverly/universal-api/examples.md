# Leverly Universal API Examples

These examples use the MindCloud API key and Leverly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create Call



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leverly/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "phone1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leverly/latest/actions/create-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "phone1": "string"
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
      "inquiryId": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Call action reference](actions/create-call.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leverly/latest/actions/create-call).
