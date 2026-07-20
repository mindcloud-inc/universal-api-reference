# EndBounce Universal API Examples

These examples use the MindCloud API key and EndBounce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Find Email

Finds an email in EndBounce by name and domain.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/find-email?connectionId=$CONNECTION_ID&name=Ava%20Chen&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/find-email?${params}`, {
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
      "found": true,
      "message": "string",
      "method": "string",
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Find Email action reference](actions/find-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/endBounce/latest/actions/find-email).

## Verify Email

Creates an email verification result in EndBounce.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/verify-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/verify-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "durationMs": 1,
      "email": "ava@example.com",
      "isCatchAll": true,
      "isDisposable": true,
      "isRole": true,
      "mode": "string",
      "reason": "string",
      "score": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Email action reference](actions/verify-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/endBounce/latest/actions/verify-email).
