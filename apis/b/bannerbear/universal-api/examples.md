# Bannerbear Universal API Examples

These examples use the MindCloud API key and Bannerbear connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authorize

Verifies API authentication with Bannerbear.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/authorize?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/authorize?${params}`, {
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

See the full [Authorize action reference](actions/authorize.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bannerbear/latest/actions/authorize).

## Create Collection

Creates a new collection in Bannerbear.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template_set": "string",
  "modifications[]": [
    {}
  ],
  "modifications[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template_set": "string",
    "modifications[]": [{}],
    "modifications[].name": "Ava Chen"
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

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bannerbear/latest/actions/create-collection).
