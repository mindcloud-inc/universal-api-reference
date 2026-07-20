# Klipfolio Universal API Examples

These examples use the MindCloud API key and Klipfolio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves the current user profile from Klipfolio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/get-profile?${params}`, {
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
      "company": {},
      "date_created": "string",
      "date_last_login": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "is_locked_out": true,
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/klipfolio/latest/actions/get-profile).
