# Glam AI Universal API Examples

These examples use the MindCloud API key and Glam AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Filters

Retrieves available filters from Glam AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-filters?${params}`, {
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
      "example_image": "string",
      "example_video": "string",
      "filter_id": "string",
      "generation_price": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Filters action reference](actions/get-filters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/glamAI/latest/actions/get-filters).

## Create Generation

Creates an image generation in Glam AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/create-generation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaUrl": "https://example.com",
  "filterName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/create-generation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaUrl": "https://example.com",
    "filterName": "Ava Chen"
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
      "event_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Generation action reference](actions/create-generation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/glamAI/latest/actions/create-generation).
