# Encharge Ingest Universal API Examples

These examples use the MindCloud API key and Encharge Ingest connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Alias Person



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/alias-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/enchargeIngest/latest/actions/alias-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user": {}
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Alias Person action reference](actions/alias-person.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/enchargeIngest/latest/actions/alias-person).
