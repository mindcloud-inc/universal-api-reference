# Sign Customiser Universal API Examples

These examples use the MindCloud API key and Sign Customiser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Webhooks

Retrieves all webhook subscriptions from Sign Customiser.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/list-webhooks?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "meta": {},
      "ownerId": 1,
      "ownerType": "string",
      "secret": "string",
      "status": "string",
      "topic": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webhookId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Webhooks action reference](actions/list-webhooks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signCustomiser/latest/actions/list-webhooks).

## Create Webhook

Creates a new webhook subscription in Sign Customiser.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topic": "form:submitted",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signCustomiser/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topic": "form:submitted",
    "url": "https://example.com"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "meta": {},
      "ownerId": 1,
      "ownerType": "string",
      "secret": "string",
      "status": "string",
      "topic": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "webhookId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signCustomiser/latest/actions/create-webhook).
