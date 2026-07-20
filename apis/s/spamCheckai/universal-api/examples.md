# SpamCheck.ai Universal API Examples

These examples use the MindCloud API key and SpamCheck.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Spam Reports

Retrieves saved spam reports from SpamCheck.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/list-spam-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/list-spam-reports?${params}`, {
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
      "admin_notes": "string",
      "admin_verified_at": "2026-05-07T12:00:00.000Z",
      "admin_verified_status": "string",
      "body": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "desired_outcome": true,
      "email": "ava@example.com",
      "external_metadata": {},
      "id": 1,
      "ip": "string",
      "notes": "string",
      "result": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Spam Reports action reference](actions/list-spam-reports.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spamCheckai/latest/actions/list-spam-reports).

## Create Spam Report

Creates a new spam report in SpamCheck.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/create-spam-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "result": true,
  "desiredOutcome": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spamCheckai/latest/actions/create-spam-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "result": true,
    "desiredOutcome": true
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
      "admin_notes": "string",
      "admin_verified_at": "2026-05-07T12:00:00.000Z",
      "admin_verified_status": "string",
      "body": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "desired_outcome": true,
      "email": "ava@example.com",
      "external_metadata": {},
      "id": 1,
      "ip": "string",
      "notes": "string",
      "result": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Spam Report action reference](actions/create-spam-report.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spamCheckai/latest/actions/create-spam-report).
