# Stability AI Universal API Examples

These examples use the MindCloud API key and Stability AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Async Generation Result

Retrieves an asynchronous generation result from Stability AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/fetch-async-generation-result?connectionId=$CONNECTION_ID&id=generation-result-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "generation-result-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/fetch-async-generation-result?${params}`, {
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
      "finish_reason": "string",
      "id": "string",
      "image": "string",
      "seed": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Fetch Async Generation Result action reference](actions/fetch-async-generation-result.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stabilityAI/latest/actions/fetch-async-generation-result).

## Conservative Upscale Image

Upscales an image in Stability AI with conservative mode.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/conservative-upscale-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stabilityAI/latest/actions/conservative-upscale-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string",
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
      "finish_reason": "string",
      "image": "string",
      "seed": 1
    }
  ],
  "meta": {}
}
```

See the full [Conservative Upscale Image action reference](actions/conservative-upscale-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stabilityAI/latest/actions/conservative-upscale-image).
