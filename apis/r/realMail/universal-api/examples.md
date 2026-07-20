# RealMail Universal API Examples

These examples use the MindCloud API key and RealMail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Email

Validates an email address with RealMail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realMail/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=email%40domain.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "email@domain.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realMail/latest/actions/validate-email?${params}`, {
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
      "free_email_provider": true,
      "has_active_website": true,
      "is_disposable": true,
      "is_suspected_role": true,
      "mx_found": true,
      "reason_code": "string",
      "reason_message": "string",
      "remaining_validations": 1,
      "suggestion": "string",
      "valid": true,
      "valid_email_format": true
    }
  ],
  "meta": {}
}
```

See the full [Validate Email action reference](actions/validate-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/realMail/latest/actions/validate-email).
