# Placker Universal API Examples

These examples use the MindCloud API key and Placker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List User Notifications



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-user-notifications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/list-user-notifications?${params}`, {
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

See the full [List User Notifications action reference](actions/list-user-notifications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/placker/latest/actions/list-user-notifications).

## Add Card Comment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placker/latest/actions/add-card-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "card": "12345",
  "content": "Please review this card."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/add-card-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "card": "12345",
    "content": "Please review this card."
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

See the full [Add Card Comment action reference](actions/add-card-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/placker/latest/actions/add-card-comment).
