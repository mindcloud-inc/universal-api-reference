# EDEN AI Universal API Examples

These examples use the MindCloud API key and EDEN AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves your available credits from EDEN AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/get-credits?${params}`, {
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
      "credits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eDENAI/latest/actions/get-credits).

## Moderate Text

Creates a text moderation request in EDEN AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/moderate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/moderate-text', {
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
  "data": [
    {
      "cost": "string",
      "error": {},
      "feature": "string",
      "originalResponse": {},
      "output": {
        "items": [
          {}
        ],
        "nsfwLikelihood": 1,
        "nsfwLikelihoodScore": 1
      },
      "provider": "string",
      "status": "string",
      "subfeature": "string"
    }
  ],
  "meta": {}
}
```

See the full [Moderate Text action reference](actions/moderate-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eDENAI/latest/actions/moderate-text).
