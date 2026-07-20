# RecurPost Universal API Examples

These examples use the MindCloud API key and RecurPost connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## User Login

Verifies RecurPost API credentials.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/user-login?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/user-login?${params}`, {
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
      "message": "string",
      "status": 1,
      "user_info": {}
    }
  ],
  "meta": {}
}
```

See the full [User Login action reference](actions/user-login.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recurPost/latest/actions/user-login).

## Add Content to Library

Creates library content in RecurPost.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/add-content-to-library" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recurPost/latest/actions/add-content-to-library', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "message": "string"
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

See the full [Add Content to Library action reference](actions/add-content-to-library.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/recurPost/latest/actions/add-content-to-library).
