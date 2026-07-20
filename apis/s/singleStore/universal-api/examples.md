# SingleStore Universal API Examples

These examples use the MindCloud API key and SingleStore connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Schedule Settings

Retrieves schedule settings from SingleStore.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/get-schedule-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/get-schedule-settings?${params}`, {
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
      "duration": 1,
      "isScheduled": true,
      "offset": 1,
      "type": "string",
      "weekFlags": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Schedule Settings action reference](actions/get-schedule-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/singleStore/latest/actions/get-schedule-settings).

## Execute an Operation in Ingest

Executes an ingest operation in SingleStore.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/execute-an-operation-in-ingest" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "operation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/execute-an-operation-in-ingest', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "operation": "string"
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Execute an Operation in Ingest action reference](actions/execute-an-operation-in-ingest.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/singleStore/latest/actions/execute-an-operation-in-ingest).
