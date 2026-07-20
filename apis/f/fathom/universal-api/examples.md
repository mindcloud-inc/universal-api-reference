# Fathom Universal API Examples

These examples use the MindCloud API key and Fathom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Meetings

Retrieves meetings from Fathom.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fathom/latest/actions/list-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fathom/latest/actions/list-meetings?${params}`, {
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
      "items": [
        {}
      ],
      "limit": 1,
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Meetings action reference](actions/list-meetings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fathom/latest/actions/list-meetings).

## Create Webhook

Creates a new webhook in Fathom.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fathom/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationUrl": "https://example.com",
  "triggeredFor[]": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fathom/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationUrl": "https://example.com",
    "triggeredFor[]": "0"
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
      "id": "string",
      "includeActionItems": true,
      "includeCrmMatches": true,
      "includeSummary": true,
      "includeTranscript": true,
      "secret": "string",
      "triggeredFor": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fathom/latest/actions/create-webhook).
