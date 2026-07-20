# OpenRouter Universal API Examples

These examples use the MindCloud API key and OpenRouter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current API Key

Retrieves the current API key from OpenRouter.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/get-current-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/get-current-api-key?${params}`, {
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

See the full [Get Current API Key action reference](actions/get-current-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openRouter/latest/actions/get-current-api-key).

## Assign Keys To Guardrail

Assigns API keys to a guardrail in OpenRouter.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/assign-keys-to-guardrail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "keyHashes[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openRouter/latest/actions/assign-keys-to-guardrail', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "keyHashes[]": ["string"]
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

See the full [Assign Keys To Guardrail action reference](actions/assign-keys-to-guardrail.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openRouter/latest/actions/assign-keys-to-guardrail).
