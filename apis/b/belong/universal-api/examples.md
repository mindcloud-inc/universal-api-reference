# Belong Universal API Examples

These examples use the MindCloud API key and Belong connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Profile

Retrieves the current user profile from Belong.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-current-user-profile?${params}`, {
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
      "biography": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": {},
      "phoneNumber": {},
      "proGaslessCollection": true,
      "username": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Profile action reference](actions/get-current-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/belong/latest/actions/get-current-user-profile).
