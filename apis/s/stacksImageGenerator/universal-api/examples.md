# 88stacks Image Generator Universal API Examples

These examples use the MindCloud API key and 88stacks Image Generator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves image generation models from 88stacks Image Generator.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-models?${params}`, {
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
      "callback": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "instancePrompt": "string",
      "invokesCount": 1,
      "keyword": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stacksImageGenerator/latest/actions/list-models).

## Create Image

Creates images in 88stacks Image Generator from a prompt.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/create-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
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
      "key": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Image action reference](actions/create-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stacksImageGenerator/latest/actions/create-image).
