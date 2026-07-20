# Email Verifier Api Universal API Examples

These examples use the MindCloud API key and Email Verifier Api connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email (GET)



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifierApi/latest/actions/verify-email-get?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailVerifierApi/latest/actions/verify-email-get?${params}`, {
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
      "details": "string",
      "domain": "string",
      "email": "ava@example.com",
      "emailSuggested": "ava@example.com",
      "error": "string",
      "event": "string",
      "execution": 1,
      "isComplainer": true,
      "isDisposable": true,
      "isFreeService": true,
      "isGibberish": true,
      "isOffensive": true,
      "isRoleAccount": true,
      "mailbox": "string",
      "mxIp": "string",
      "mxLocation": "string",
      "possibleSpamtrap": true,
      "remaining": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Email (GET) action reference](actions/verify-email-get.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailVerifierApi/latest/actions/verify-email-get).

## Verify Email (POST)



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailVerifierApi/latest/actions/verify-email-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "name@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailVerifierApi/latest/actions/verify-email-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "name@example.com"
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
      "details": "string",
      "domain": "string",
      "email": "ava@example.com",
      "emailSuggested": "ava@example.com",
      "error": "string",
      "event": "string",
      "execution": 1,
      "isComplainer": true,
      "isDisposable": true,
      "isFreeService": true,
      "isGibberish": true,
      "isOffensive": true,
      "isRoleAccount": true,
      "mailbox": "string",
      "mxIp": "string",
      "mxLocation": "string",
      "possibleSpamtrap": true,
      "remaining": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Email (POST) action reference](actions/verify-email-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailVerifierApi/latest/actions/verify-email-post).
