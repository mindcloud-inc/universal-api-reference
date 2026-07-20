# GoZen DeepAgent Universal API Examples

These examples use the MindCloud API key and GoZen DeepAgent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves your GoZen DeepAgent user profile.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/get-profile?${params}`, {
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
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goZenDeepAgent/latest/actions/get-profile).

## Register Webhook

Registers a webhook in GoZen DeepAgent.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/register-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "knowledgebaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goZenDeepAgent/latest/actions/register-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "knowledgebaseId": "string"
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
      "integrationId": "string",
      "knowledgebaseId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Register Webhook action reference](actions/register-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goZenDeepAgent/latest/actions/register-webhook).
