# Client Commander Universal API Examples

These examples use the MindCloud API key and Client Commander connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Client Commander.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientCommander/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clientCommander/latest/actions/get-current-user?${params}`, {
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
      "data": {
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "role": "string",
        "teams": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      },
      "meta": {
        "requestId": "string",
        "timestamp": "string",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clientCommander/latest/actions/get-current-user).
