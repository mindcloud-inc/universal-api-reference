# Flotiq Universal API Examples

These examples use the MindCloud API key and Flotiq connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Auth Context

Retrieves your current Flotiq authentication context.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-auth-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-auth-context?${params}`, {
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
      "organization": {},
      "space": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Auth Context action reference](actions/get-auth-context.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flotiq/latest/actions/get-auth-context).

## Archive Content Object

Archives a content object in Flotiq.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/archive-content-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/archive-content-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "id": "string"
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

See the full [Archive Content Object action reference](actions/archive-content-object.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flotiq/latest/actions/archive-content-object).
