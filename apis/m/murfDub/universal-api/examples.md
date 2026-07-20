# Murf Dub Universal API Examples

These examples use the MindCloud API key and Murf Dub connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Destination Languages

Retrieves destination languages from Murf Dub.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-destination-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/list-destination-languages?${params}`, {
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
      "language": "string",
      "locale": "string",
      "supports": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Destination Languages action reference](actions/list-destination-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/murfDub/latest/actions/list-destination-languages).

## Create Dubbing Job

Creates a dubbing job in Murf Dub.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/create-dubbing-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetLocales": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/murfDub/latest/actions/create-dubbing-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetLocales": "string"
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
      "dubbing_type": "string",
      "file_name": "Ava Chen",
      "file_url": "https://example.com",
      "job_id": "string",
      "priority": "string",
      "source_locale": "string",
      "target_locales": [
        "string"
      ],
      "warning": "string",
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Dubbing Job action reference](actions/create-dubbing-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/murfDub/latest/actions/create-dubbing-job).
