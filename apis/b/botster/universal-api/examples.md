# Botster Universal API Examples

These examples use the MindCloud API key and Botster connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves your remaining Botster credits balance.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botster/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botster/latest/actions/get-credits?${params}`, {
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
      "credits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botster/latest/actions/get-credits).

## Archive Job

Archives an existing job in Botster.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botster/latest/actions/archive-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botster/latest/actions/archive-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string"
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
      "archived": true,
      "job": {
        "bot": {
          "id": "string",
          "name": "Ava Chen"
        },
        "finished": true,
        "id": "string",
        "name": "Ava Chen",
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Archive Job action reference](actions/archive-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botster/latest/actions/archive-job).
