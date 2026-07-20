# QuickEmailVerification Universal API Examples

These examples use the MindCloud API key and QuickEmailVerification connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email in Sandbox Mode

Retrieves a simulated email verification result from QuickEmailVerification.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email-in-sandbox-mode?connectionId=$CONNECTION_ID&email=safe-to-send%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "safe-to-send@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickEmailVerification/latest/actions/verify-email-in-sandbox-mode?${params}`, {
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
      "accept_all": "string",
      "did_you_mean": "string",
      "disposable": "string",
      "domain": "string",
      "email": "ava@example.com",
      "free": "string",
      "message": "string",
      "reason": "string",
      "result": "string",
      "role": "string",
      "safe_to_send": "string",
      "success": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Email in Sandbox Mode action reference](actions/verify-email-in-sandbox-mode.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quickEmailVerification/latest/actions/verify-email-in-sandbox-mode).
