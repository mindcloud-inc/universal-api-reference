# Mixpanel Universal API Examples

These examples use the MindCloud API key and Mixpanel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Export Events

Retrieves raw events from Mixpanel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/export-events?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/export-events?${params}`, {
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

See the full [Export Events action reference](actions/export-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mixpanel/latest/actions/export-events).

## Append to Profile List Property

Appends values to a user profile list in Mixpanel.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/append-to-profile-list-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "distinctId": "user_123",
  "append": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/append-to-profile-list-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "distinctId": "user_123",
    "append": "[object Object]"
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
      "response": 1
    }
  ],
  "meta": {}
}
```

See the full [Append to Profile List Property action reference](actions/append-to-profile-list-property.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mixpanel/latest/actions/append-to-profile-list-property).
