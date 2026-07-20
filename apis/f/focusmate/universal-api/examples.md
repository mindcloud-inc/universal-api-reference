# Focusmate Universal API Examples

These examples use the MindCloud API key and Focusmate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile

Retrieves your personal Focusmate profile data.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-my-profile?${params}`, {
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
      "user": {
        "email": "ava@example.com",
        "memberSince": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "photoUrl": "https://example.com",
        "timeZone": "string",
        "totalSessionCount": 1,
        "userId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/focusmate/latest/actions/get-my-profile).
