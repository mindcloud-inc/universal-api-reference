# Acumbamail Universal API Examples

These examples use the MindCloud API key and Acumbamail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists

Retrieves available subscriber lists from Acumbamail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/list-lists?${params}`, {
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

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/acumbamail/latest/actions/list-lists).

## Add Subscriber

Creates a subscriber in an Acumbamail list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/add-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/add-subscriber', {
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

See the full [Add Subscriber action reference](actions/add-subscriber.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/acumbamail/latest/actions/add-subscriber).
