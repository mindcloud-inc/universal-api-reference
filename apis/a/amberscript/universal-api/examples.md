# Amberscript Universal API Examples

These examples use the MindCloud API key and Amberscript connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Jobs

Retrieves jobs from your Amberscript account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/list-jobs?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "jobId": "string",
      "jobOptions": {
        "anonymization": "string",
        "burnInSubtitles": true,
        "dresingPehl": true,
        "extendedDelivery": "string",
        "portal": true,
        "timestampEnabledInExport": true
      },
      "jobType": "string",
      "language": "string",
      "nrAudioSeconds": 1,
      "status": "string",
      "transcriptionType": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Jobs action reference](actions/list-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amberscript/latest/actions/list-jobs).

## Create Glossary

Creates a new glossary in Amberscript.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/create-glossary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/create-glossary', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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

See the full [Create Glossary action reference](actions/create-glossary.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amberscript/latest/actions/create-glossary).
