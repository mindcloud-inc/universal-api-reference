# Pencil Spaces Universal API Examples

These examples use the MindCloud API key and Pencil Spaces connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Custom Attributes



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-custom-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/list-custom-attributes?${params}`, {
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

See the full [List Custom Attributes action reference](actions/list-custom-attributes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pencilSpaces/latest/actions/list-custom-attributes).

## Create Event



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/create-event', {
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

See the full [Create Event action reference](actions/create-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pencilSpaces/latest/actions/create-event).
