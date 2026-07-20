# 3Scribe Universal API Examples

These examples use the MindCloud API key and 3Scribe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Transcription Jobs

Retrieves transcription jobs from your 3Scribe account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scribe/latest/actions/list-transcription-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scribe/latest/actions/list-transcription-jobs?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Transcription Jobs action reference](actions/list-transcription-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scribe/latest/actions/list-transcription-jobs).

## Create Transcription Job Via Pre-Signed URL

Creates a new transcription job in 3Scribe from a pre-signed upload URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scribe/latest/actions/create-transcription-job-via-pre-signed-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "requestUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scribe/latest/actions/create-transcription-job-via-pre-signed-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "requestUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Transcription Job Via Pre-Signed URL action reference](actions/create-transcription-job-via-pre-signed-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scribe/latest/actions/create-transcription-job-via-pre-signed-url).
