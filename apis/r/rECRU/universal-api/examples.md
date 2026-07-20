# RECRU Universal API Examples

These examples use the MindCloud API key and RECRU connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Echo Text



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/echo-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/echo-text?${params}`, {
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

See the full [Echo Text action reference](actions/echo-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rECRU/latest/actions/echo-text).

## Add Newsletter Unsubscribe



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/add-newsletter-unsubscribe" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rECRU/latest/actions/add-newsletter-unsubscribe', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add Newsletter Unsubscribe action reference](actions/add-newsletter-unsubscribe.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rECRU/latest/actions/add-newsletter-unsubscribe).
