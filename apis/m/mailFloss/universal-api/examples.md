# MailFloss Universal API Examples

These examples use the MindCloud API key and MailFloss connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email Address

Verifies an email address with MailFloss.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/verify-email-address?${params}`, {
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
      "disposable": true,
      "domain": "string",
      "email": "ava@example.com",
      "free": true,
      "meta": "string",
      "passed": true,
      "reason": "string",
      "role": true,
      "status": "string",
      "suggestion": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Email Address action reference](actions/verify-email-address.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailFloss/latest/actions/verify-email-address).

## Cancel Batch Verification Job

Cancels a batch email verification job in MailFloss.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/cancel-batch-verification-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/cancel-batch-verification-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Batch Verification Job action reference](actions/cancel-batch-verification-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailFloss/latest/actions/cancel-batch-verification-job).
