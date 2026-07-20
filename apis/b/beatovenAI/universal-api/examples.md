# Beatoven AI Universal API Examples

These examples use the MindCloud API key and Beatoven AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Task Status

Retrieves composition task status from Beatoven AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/get-task-status?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/get-task-status?${params}`, {
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
      "meta": {
        "duration": 1,
        "prompt": {
          "text": "string"
        },
        "stems_url": {
          "bass": "https://example.com",
          "chords": "https://example.com",
          "melody": "https://example.com",
          "percussion": "https://example.com"
        },
        "track_id": "string",
        "track_url": "https://example.com"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Task Status action reference](actions/get-task-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beatovenAI/latest/actions/get-task-status).

## Compose Track

Starts track composition in Beatoven AI from a text prompt.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/compose-track" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt.text": "5 seconds soft piano note"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beatovenAI/latest/actions/compose-track', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt.text": "5 seconds soft piano note"
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
      "status": "string",
      "task_id": "string",
      "track_id": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Compose Track action reference](actions/compose-track.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beatovenAI/latest/actions/compose-track).
