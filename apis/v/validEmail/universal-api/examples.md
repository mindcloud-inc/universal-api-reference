# ValidEmail Universal API Examples

These examples use the MindCloud API key and ValidEmail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email

Verifies an email address with ValidEmail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validEmail/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validEmail/latest/actions/verify-email?${params}`, {
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
      "AcceptAll": true,
      "Disposable": true,
      "Domain": "string",
      "Email": "ava@example.com",
      "EmailAdditionalInfo": [
        {}
      ],
      "Free": true,
      "IsValid": true,
      "MXRecord": "string",
      "Reason": "string",
      "Role": true,
      "Score": 1,
      "State": "string",
      "Tag": true
    }
  ],
  "meta": {}
}
```

See the full [Verify Email action reference](actions/verify-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/validEmail/latest/actions/verify-email).
