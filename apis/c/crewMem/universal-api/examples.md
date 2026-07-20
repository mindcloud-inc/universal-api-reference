# CrewMem Universal API Examples

These examples use the MindCloud API key and CrewMem connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Memory Jobs



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/list-memory-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/list-memory-jobs?${params}`, {
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
      "data": {},
      "limit": 1,
      "offset": 1,
      "pendingCount": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Memory Jobs action reference](actions/list-memory-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crewMem/latest/actions/list-memory-jobs).

## Add Memory



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/add-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "inputData": "string",
  "teamName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/add-memory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "inputData": "string",
    "teamName": "Ava Chen"
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
      "addedMemoryCount": 1,
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Memory action reference](actions/add-memory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/crewMem/latest/actions/add-memory).
