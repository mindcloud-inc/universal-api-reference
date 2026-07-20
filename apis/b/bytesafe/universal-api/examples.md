# Bytesafe Universal API Examples

These examples use the MindCloud API key and Bytesafe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from your Bytesafe workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bytesafe/latest/actions/get-authenticated-user?${params}`, {
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
      "email": "ava@example.com",
      "groups": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "organizationId": "string",
      "plan": "string",
      "role": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bytesafe/latest/actions/get-authenticated-user).
