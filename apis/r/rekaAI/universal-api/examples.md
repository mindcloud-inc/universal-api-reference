# Reka AI Universal API Examples

These examples use the MindCloud API key and Reka AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves models from Reka AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-models?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rekaAI/latest/actions/list-models).

## Ask Video QA

Creates a video QA response in Reka AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/ask-video-qa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/ask-video-qa', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video_id": "string"
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
      "choices": [
        {}
      ],
      "id": "string",
      "model": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Ask Video QA action reference](actions/ask-video-qa.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rekaAI/latest/actions/ask-video-qa).
