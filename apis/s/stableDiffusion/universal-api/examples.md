# Stable Diffusion Universal API Examples

These examples use the MindCloud API key and Stable Diffusion connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves account balance from Stable Diffusion.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/get-balance?${params}`, {
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

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stableDiffusion/latest/actions/get-balance).

## Control Sketch Image

Generates an image from a sketch in Stable Diffusion.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/control-sketch-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stableDiffusion/latest/actions/control-sketch-image', {
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

See the full [Control Sketch Image action reference](actions/control-sketch-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stableDiffusion/latest/actions/control-sketch-image).
