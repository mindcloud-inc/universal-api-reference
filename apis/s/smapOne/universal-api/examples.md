# smapOne Universal API Examples

These examples use the MindCloud API key and smapOne connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List smaps

Retrieves smaps from smapOne.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smaps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/list-smaps?${params}`, {
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
      "lastPublishedVersion": {},
      "name": "Ava Chen",
      "smapId": "string",
      "totalDataCount": 1,
      "totalOpenTasksCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List smaps action reference](actions/list-smaps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smapOne/latest/actions/list-smaps).

## Create task

Creates a new task in smapOne.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "smap_id": "string",
  "title": "string",
  "version": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "smap_id": "string",
    "title": "string",
    "version": "string"
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
      "id": "string",
      "recordType": "string",
      "userEmail": "ava@example.com",
      "userName": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create task action reference](actions/create-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smapOne/latest/actions/create-task).
