# Airmeet Universal API Examples

These examples use the MindCloud API key and Airmeet connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Airmeets

Finds Airmeet events accessible to your token.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-airmeets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-airmeets?${params}`, {
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

See the full [List Airmeets action reference](actions/list-airmeets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airmeet/latest/actions/list-airmeets).

## Add Authorized Attendee

Creates an authorized attendee in Airmeet.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/add-authorized-attendee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "airmeetId": "string",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/add-authorized-attendee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "airmeetId": "string",
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
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

See the full [Add Authorized Attendee action reference](actions/add-authorized-attendee.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airmeet/latest/actions/add-authorized-attendee).
