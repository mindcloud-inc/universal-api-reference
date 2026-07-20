# Opportify Universal API Examples

These examples use the MindCloud API key and Opportify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Analyze Email

Analyzes an email address in Opportify for deliverability and risk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-email?${params}`, {
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
      "addressSignals": {},
      "domain": {},
      "emailAddress": "ava@example.com",
      "emailAutoCorrectedFrom": "ava@example.com",
      "emailCorrection": "ava@example.com",
      "emailDNS": {},
      "emailProvider": "ava@example.com",
      "emailType": "ava@example.com",
      "isCatchAll": true,
      "isDeliverable": "string",
      "isFormatValid": true,
      "isMailboxFull": true,
      "isReachable": true,
      "riskReport": {}
    }
  ],
  "meta": {}
}
```

See the full [Analyze Email action reference](actions/analyze-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/opportify/latest/actions/analyze-email).

## Batch Analyze Emails

Creates an asynchronous email analysis job in Opportify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/batch-analyze-emails" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/opportify/latest/actions/batch-analyze-emails', {
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
      "jobId": "string",
      "name": "Ava Chen",
      "status": "string",
      "statusDescription": "string"
    }
  ],
  "meta": {}
}
```

See the full [Batch Analyze Emails action reference](actions/batch-analyze-emails.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/opportify/latest/actions/batch-analyze-emails).
