# API Labz Universal API Examples

These examples use the MindCloud API key and API Labz connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Email Validator

Validates an email address with API Labz.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/email-validator?connectionId=$CONNECTION_ID&emailAddress=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/email-validator?${params}`, {
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
      "autocorrect": "string",
      "deliverability": "string",
      "email": "ava@example.com",
      "isCatchallEmail": {
        "text": "ava@example.com",
        "value": true
      },
      "isDisposableEmail": {
        "text": "ava@example.com",
        "value": true
      },
      "isFreeEmail": {
        "text": "ava@example.com",
        "value": true
      },
      "isMxFound": {
        "text": "string",
        "value": true
      },
      "isRoleEmail": {
        "text": "ava@example.com",
        "value": true
      },
      "isSmtpValid": {
        "text": "string",
        "value": true
      },
      "isValidFormat": {
        "text": "string",
        "value": true
      },
      "qualityScore": "string"
    }
  ],
  "meta": {}
}
```

See the full [Email Validator action reference](actions/email-validator.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aPILabz/latest/actions/email-validator).
