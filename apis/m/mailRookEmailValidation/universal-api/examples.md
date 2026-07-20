# MailRook Email Validation Universal API Examples

These examples use the MindCloud API key and MailRook Email Validation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Email

Validates an email address in MailRook.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/validate-email?${params}`, {
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
      "code": 1,
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Email action reference](actions/validate-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailRookEmailValidation/latest/actions/validate-email).

## Submit Validation Batch

Submits a batch of email addresses for validation in MailRook.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/submit-validation-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/submit-validation-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Submit Validation Batch action reference](actions/submit-validation-batch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailRookEmailValidation/latest/actions/submit-validation-batch).
