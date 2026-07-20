# EmailVerify.io Universal API Examples

These examples use the MindCloud API key and EmailVerify.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Email

Validates an email address with EmailVerify.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/validate-email?${params}`, {
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
      "status": "string",
      "subStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Email action reference](actions/validate-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailVerifyio/latest/actions/validate-email).

## Start Bulk Verification Task

Creates a bulk verification task in EmailVerify.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/start-bulk-verification-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "emailBatch": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/start-bulk-verification-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "emailBatch": {}
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
      "countDuplicatesRemoved": 1,
      "countProcessing": 1,
      "countRejectedEmails": 1,
      "countSubmitted": 1,
      "status": "string",
      "taskId": 1
    }
  ],
  "meta": {}
}
```

See the full [Start Bulk Verification Task action reference](actions/start-bulk-verification-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailVerifyio/latest/actions/start-bulk-verification-task).
