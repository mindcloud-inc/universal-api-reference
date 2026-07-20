# Landingi Universal API Examples

These examples use the MindCloud API key and Landingi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Programmatic Processes

Retrieves programmatic landing page processes from Landingi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-programmatic-processes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-programmatic-processes?${params}`, {
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
      "created_at": "string",
      "errors": 1,
      "identifier": "string",
      "name": "Ava Chen",
      "processed": 1,
      "source_archived": true,
      "source_uuid": "string",
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Programmatic Processes action reference](actions/list-programmatic-processes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/landingi/latest/actions/list-programmatic-processes).

## Start Programmatic Process

Starts a programmatic landing page process in Landingi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/landingi/latest/actions/start-programmatic-process" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceLandingPageUuid": "string",
  "name": "Ava Chen",
  "immediatePublication": true,
  "variants[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/landingi/latest/actions/start-programmatic-process', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceLandingPageUuid": "string",
    "name": "Ava Chen",
    "immediatePublication": true,
    "variants[]": [{}]
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
      "process_identifier": "string"
    }
  ],
  "meta": {}
}
```

See the full [Start Programmatic Process action reference](actions/start-programmatic-process.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/landingi/latest/actions/start-programmatic-process).
