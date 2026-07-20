# Segmind Universal API Examples

These examples use the MindCloud API key and Segmind connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download Fine-Tuned Model File



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/download-fine-tuned-model-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/segmind/latest/actions/download-fine-tuned-model-file?${params}`, {
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
      "expiresAt": "string",
      "fileUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Download Fine-Tuned Model File action reference](actions/download-fine-tuned-model-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/segmind/latest/actions/download-fine-tuned-model-file).

## Add Dedicated Endpoint



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/segmind/latest/actions/add-dedicated-endpoint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/segmind/latest/actions/add-dedicated-endpoint', {
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
      "endpointId": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Dedicated Endpoint action reference](actions/add-dedicated-endpoint.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/segmind/latest/actions/add-dedicated-endpoint).
