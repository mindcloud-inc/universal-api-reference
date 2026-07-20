# Sniffmail Universal API Examples

These examples use the MindCloud API key and Sniffmail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Credentials

Validates Sniffmail credentials with a test email verification request.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/validate-credentials?${params}`, {
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
      "is_deliverable": true,
      "is_disposable": true,
      "is_reachable": "string",
      "is_role_account": true,
      "is_valid": true,
      "mx_valid": true,
      "reason": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Credentials action reference](actions/validate-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sniffmail/latest/actions/validate-credentials).

## Create Bulk Job

Creates a bulk email verification job in Sniffmail.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/create-bulk-job" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/create-bulk-job', {
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
      "message": "string",
      "status": "string",
      "totalEmails": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Job action reference](actions/create-bulk-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sniffmail/latest/actions/create-bulk-job).
