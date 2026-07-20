# Handelsregister AI Universal API Examples

These examples use the MindCloud API key and Handelsregister AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Organizations

Finds organizations in Handelsregister AI by search query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/search-organizations?connectionId=$CONNECTION_ID&q=BMW%20AG" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "BMW AG"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/search-organizations?${params}`, {
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
      "meta": {},
      "results": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Search Organizations action reference](actions/search-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/handelsregisterAI/latest/actions/search-organizations).

## Create API Token

Creates a new API token in Handelsregister AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/create-api-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tokenName": "codex-temp-token"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/create-api-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tokenName": "codex-temp-token"
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
      "abilities": [
        "string"
      ],
      "created_at": "string",
      "expires_at": "string",
      "meta": {},
      "name": "Ava Chen",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create API Token action reference](actions/create-api-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/handelsregisterAI/latest/actions/create-api-token).
