# ContactOut Universal API Examples

These examples use the MindCloud API key and ContactOut connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Usage Stats

Retrieves API usage stats for a month in ContactOut.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-api-usage-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-api-usage-stats?${params}`, {
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
      "message": "string",
      "period": {
        "end": "string",
        "start": "string"
      },
      "status_code": 1,
      "usage": {
        "count": 1,
        "over_quota": 1,
        "phone_count": 1,
        "phone_over_quota": 1,
        "phone_quota": 1,
        "phone_remaining": 1,
        "quota": 1,
        "remaining": 1,
        "search_count": 1,
        "search_over_quota": 1,
        "search_quota": 1,
        "search_remaining": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get API Usage Stats action reference](actions/get-api-usage-stats.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contactOut/latest/actions/get-api-usage-stats).

## Queue Batch Email Verification

Creates a batch email verification job in ContactOut.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/queue-batch-email-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/queue-batch-email-verification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": "ava@example.com"
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
      "job_id": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Queue Batch Email Verification action reference](actions/queue-batch-email-verification.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contactOut/latest/actions/queue-batch-email-verification).
