# Slottable Universal API Examples

These examples use the MindCloud API key and Slottable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Token Details

Retrieves API token details from Slottable.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slottable/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slottable/latest/actions/get-token-details?${params}`, {
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
      "attributes": {
        "company_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "name": "Ava Chen"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Token Details action reference](actions/get-token-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/slottable/latest/actions/get-token-details).

## Create Webhook

Creates a new webhook in Slottable.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slottable/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "data.url": "https://example.com/webhooks/slottable",
  "data.model": "Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slottable/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "data.url": "https://example.com/webhooks/slottable",
    "data.model": "Contact"
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
      "attributes": {
        "company_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "events": [
          "string"
        ],
        "filter_key": "string",
        "id": 1,
        "method": "string",
        "model": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/slottable/latest/actions/create-webhook).
