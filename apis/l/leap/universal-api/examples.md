# Leap Universal API Examples

These examples use the MindCloud API key and Leap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Company Trades

Retrieves company trade records from Leap.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leap/latest/actions/list-company-trades?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leap/latest/actions/list-company-trades?${params}`, {
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
      "data": [
        {}
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [List Company Trades action reference](actions/list-company-trades.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leap/latest/actions/list-company-trades).

## Add Job Note

Creates a new note for a job in Leap.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leap/latest/actions/add-job-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": 1,
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leap/latest/actions/add-job-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": 1,
    "note": "string"
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
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Job Note action reference](actions/add-job-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leap/latest/actions/add-job-note).
