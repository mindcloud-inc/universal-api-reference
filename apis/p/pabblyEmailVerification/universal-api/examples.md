# Pabbly Email Verification Universal API Examples

These examples use the MindCloud API key and Pabbly Email Verification connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Single Email



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyEmailVerification/latest/actions/verify-single-email?connectionId=$CONNECTION_ID&email=johnfabric%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "johnfabric@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyEmailVerification/latest/actions/verify-single-email?${params}`, {
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
        "accept_all": 1,
        "disposable": 1,
        "domain": "string",
        "email": "ava@example.com",
        "free_email": 1,
        "message": "string",
        "result": "string",
        "role": 1,
        "spamtrap": 1,
        "success": true,
        "user": "string"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Single Email action reference](actions/verify-single-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pabblyEmailVerification/latest/actions/verify-single-email).
