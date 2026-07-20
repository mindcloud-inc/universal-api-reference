# Mailcheck Universal API Examples

These examples use the MindCloud API key and Mailcheck connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/get-account?${params}`, {
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
      "api_key": {
        "created_at": "string",
        "last_used_at": "string",
        "prefix": "string"
      },
      "email": "ava@example.com",
      "monthly_limit": 1,
      "plan": "string",
      "usage": {
        "current_month": 1,
        "remaining": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailcheck/latest/actions/get-account).

## Bulk Verify Emails



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/bulk-verify-emails" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/bulk-verify-emails', {
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
      "credits_remaining": 1,
      "job_id": "string",
      "results": [
        [
          {}
        ]
      ],
      "total": 1,
      "unique_verified": 1
    }
  ],
  "meta": {}
}
```

See the full [Bulk Verify Emails action reference](actions/bulk-verify-emails.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailcheck/latest/actions/bulk-verify-emails).
