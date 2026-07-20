# verifi.email Universal API Examples

These examples use the MindCloud API key and verifi.email connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Email

Validate a single email address and return deliverability checks, including syntax, MX, spoofing, and disposable-provider details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/validate-email?${params}`, {
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
      "details": {
        "disposable": true,
        "mx": {
          "provider": "string",
          "records": [
            "string"
          ]
        },
        "rfcCompliant": true,
        "spoofFree": true,
        "validMxRecord": true
      },
      "email": "ava@example.com",
      "valid": true
    }
  ],
  "meta": {}
}
```

See the full [Validate Email action reference](actions/validate-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verifiemail/latest/actions/validate-email).
