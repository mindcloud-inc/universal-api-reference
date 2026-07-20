# Patreon Universal API Examples

These examples use the MindCloud API key and Patreon connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Identity

Retrieves the authenticated user's profile from Patreon.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/patreon/latest/actions/get-identity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/patreon/latest/actions/get-identity?${params}`, {
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
      "data": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Identity action reference](actions/get-identity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/patreon/latest/actions/get-identity).

## Create Webhook

Creates a webhook for the current Patreon campaign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/patreon/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "triggers[]": [
    "string"
  ],
  "uri": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/patreon/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "triggers[]": ["string"],
    "uri": "string"
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
      "data": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/patreon/latest/actions/create-webhook).
