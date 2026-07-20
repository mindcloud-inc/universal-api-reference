# ModelsLab Universal API Examples

These examples use the MindCloud API key and ModelsLab connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Processing Requests

Retrieves processing request counts from ModelsLab.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/check-processing-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/check-processing-requests?${params}`, {
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
      "message": "string",
      "processing_count": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Processing Requests action reference](actions/check-processing-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/modelsLab/latest/actions/check-processing-requests).

## Caption Image

Creates an image caption in ModelsLab.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/caption-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelsLab/latest/actions/caption-image', {
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
      "generationTime": 1,
      "id": 1,
      "meta": {},
      "output": [
        "string"
      ],
      "proxy_links": [
        "https://example.com"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Caption Image action reference](actions/caption-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/modelsLab/latest/actions/caption-image).
