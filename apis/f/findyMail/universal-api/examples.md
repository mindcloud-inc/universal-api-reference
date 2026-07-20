# FindyMail Universal API Examples

These examples use the MindCloud API key and FindyMail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email

Verifies an email address with FindyMail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=john%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "john@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/verify-email?${params}`, {
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
      "provider": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

See the full [Verify Email action reference](actions/verify-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/findyMail/latest/actions/verify-email).
