# Galileo Universal API Examples

These examples use the MindCloud API key and Galileo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Galileo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-current-user?${params}`, {
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
      "authMethod": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailIsVerified": true,
      "firstName": "Ava",
      "genericPermissions": [
        {
          "action": "string",
          "allowed": true,
          "message": "string",
          "resource": "string"
        }
      ],
      "id": "string",
      "lastName": "Chen",
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "permissions": [
        {
          "action": "string",
          "allowed": true,
          "message": "string"
        }
      ],
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/galileo/latest/actions/get-current-user).
