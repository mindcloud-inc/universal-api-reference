# Valyu Universal API Examples

These examples use the MindCloud API key and Valyu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Datasources



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/list-datasources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/valyu/latest/actions/list-datasources?${params}`, {
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
      "category": "string",
      "coverage": {},
      "description": "string",
      "exampleQueries": [
        "string"
      ],
      "id": "string",
      "languages": [
        "string"
      ],
      "modality": [
        "string"
      ],
      "name": "Ava Chen",
      "pricing": {},
      "responseSchema": {},
      "size": 1,
      "source": "string",
      "topics": [
        "string"
      ],
      "type": "string",
      "updateFrequency": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Datasources action reference](actions/list-datasources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/valyu/latest/actions/list-datasources).

## Create Contents Job



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/create-contents-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": "Add one or more HTTPS URLs"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/valyu/latest/actions/create-contents-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": "Add one or more HTTPS URLs"
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
      "jobId": "string",
      "pollUrl": "https://example.com",
      "status": "string",
      "success": true,
      "txId": "string",
      "urlsTotal": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Contents Job action reference](actions/create-contents-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/valyu/latest/actions/create-contents-job).
