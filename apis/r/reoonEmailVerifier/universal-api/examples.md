# Reoon Email Verifier Universal API Examples

These examples use the MindCloud API key and Reoon Email Verifier connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Account Balance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/check-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/check-account-balance?${params}`, {
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
      "api_status": "string",
      "remaining_daily_credits": 1,
      "remaining_instant_credits": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Account Balance action reference](actions/check-account-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reoonEmailVerifier/latest/actions/check-account-balance).

## Create Bulk Verification Task



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/create-bulk-verification-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reoonEmailVerifier/latest/actions/create-bulk-verification-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails": {}
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
      "count_duplicates_removed": 1,
      "count_processing": 1,
      "count_rejected_emails": 1,
      "count_submitted": 1,
      "status": "string",
      "task_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Verification Task action reference](actions/create-bulk-verification-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reoonEmailVerifier/latest/actions/create-bulk-verification-task).
