# Vero Universal API Examples

These examples use the MindCloud API key and Vero connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Trigger

Retrieves a trigger record from Vero.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vero/latest/actions/get-trigger?connectionId=$CONNECTION_ID&id=trigger_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "trigger_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vero/latest/actions/get-trigger?${params}`, {
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
      "id": "string",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Trigger action reference](actions/get-trigger.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vero/latest/actions/get-trigger).

## Alias

Aliases an existing user record in Vero.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vero/latest/actions/alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "new_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vero/latest/actions/alias', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "new_id": "string"
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
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Alias action reference](actions/alias.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vero/latest/actions/alias).
