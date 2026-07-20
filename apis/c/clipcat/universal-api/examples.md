# Clipcat Universal API Examples

These examples use the MindCloud API key and Clipcat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authorization Status

Retrieves authorization status for the current Clipcat workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-authorization-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/get-authorization-status?${params}`, {
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
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Authorization Status action reference](actions/get-authorization-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clipcat/latest/actions/get-authorization-status).

## Create Render

Creates a new video render request in Clipcat.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/create-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modifications[]": [
    {
      "text": "Validator test",
      "scene": "Scene 1",
      "object": "_sample_object"
    }
  ],
  "template": "sample-template-uid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/create-render', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modifications[]": [{"text":"Validator test","scene":"Scene 1","object":"_sample_object"}],
    "template": "sample-template-uid"
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
      "created_at": "string",
      "credits": 1,
      "metadata": "string",
      "modifications": [
        {}
      ],
      "progress": 1,
      "self": "string",
      "status": "string",
      "template": "string",
      "uid": "string",
      "url": "https://example.com",
      "webhook_response_code": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Render action reference](actions/create-render.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clipcat/latest/actions/create-render).
