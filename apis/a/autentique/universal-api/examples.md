# Autentique Universal API Examples

These examples use the MindCloud API key and Autentique connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Current User

Retrieves the current user from Autentique.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autentique/latest/actions/fetch-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autentique/latest/actions/fetch-current-user?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "organization": {
        "id": 1,
        "name": "Ava Chen",
        "uuid": "string"
      },
      "subscription": {
        "credits": 1,
        "documents": 1,
        "hasPremiumFeatures": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Fetch Current User action reference](actions/fetch-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/autentique/latest/actions/fetch-current-user).
