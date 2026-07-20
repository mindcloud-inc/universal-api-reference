# Kickbox Universal API Examples

These examples use the MindCloud API key and Kickbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email

Verifies an email address with Kickbox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/verify-email?${params}`, {
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
      "accept_all": true,
      "did_you_mean": "string",
      "disposable": true,
      "domain": "string",
      "email": "ava@example.com",
      "free": true,
      "message": "string",
      "reason": "string",
      "result": "string",
      "role": true,
      "sendex": 1,
      "success": true,
      "user": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Email action reference](actions/verify-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kickbox/latest/actions/verify-email).

## Start Batch Verification

Starts a batch email verification job in Kickbox.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/start-batch-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kickbox/latest/actions/start-batch-verification', {
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
      "id": 1,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Start Batch Verification action reference](actions/start-batch-verification.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kickbox/latest/actions/start-batch-verification).
