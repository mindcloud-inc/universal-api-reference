# Speech is Cheap Universal API Examples

These examples use the MindCloud API key and Speech is Cheap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Health

Retrieves Speech is Cheap API health status.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/get-api-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/get-api-health?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get API Health action reference](actions/get-api-health.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/speechIsCheap/latest/actions/get-api-health).

## Create Transcription Job

Creates a new transcription job in Speech is Cheap.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/create-transcription-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputUrl": "https://example.com/audio-file.mp3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/create-transcription-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputUrl": "https://example.com/audio-file.mp3"
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
      "id": "string",
      "output": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Transcription Job action reference](actions/create-transcription-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/speechIsCheap/latest/actions/create-transcription-job).
