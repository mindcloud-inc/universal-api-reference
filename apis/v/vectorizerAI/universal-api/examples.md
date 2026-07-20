# Vectorizer AI Universal API Examples

These examples use the MindCloud API key and Vectorizer AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Account Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/account-status?${params}`, {
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
      "credits": 1,
      "subscriptionPlan": "string",
      "subscriptionState": "string"
    }
  ],
  "meta": {}
}
```

See the full [Account Status action reference](actions/account-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vectorizerAI/latest/actions/account-status).

## Vectorize



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/vectorize" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectorizerAI/latest/actions/vectorize', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Vectorize action reference](actions/vectorize.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vectorizerAI/latest/actions/vectorize).
