# Anyleads Universal API Examples

These examples use the MindCloud API key and Anyleads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Email State

Retrieves email verification status from Anyleads.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/verify-email-state?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/verify-email-state?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Verify Email State action reference](actions/verify-email-state.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anyleads/latest/actions/verify-email-state).

## Add Domain Unsubscribe

Creates a domain unsubscribe entry in Anyleads.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/add-domain-unsubscribe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/add-domain-unsubscribe', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Domain Unsubscribe action reference](actions/add-domain-unsubscribe.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anyleads/latest/actions/add-domain-unsubscribe).
