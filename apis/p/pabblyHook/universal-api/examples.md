# Pabbly Hook Universal API Examples

These examples use the MindCloud API key and Pabbly Hook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Folders



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-folders?${params}`, {
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
      "connectionCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "name": "Ava Chen",
      "sortOrder": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get All Folders action reference](actions/get-all-folders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pabblyHook/latest/actions/get-all-folders).

## Create Connection



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Payment webhook",
  "folderId": "67592783069f7717b89ba992",
  "source": {},
  "destination": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-connection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Payment webhook",
    "folderId": "67592783069f7717b89ba992",
    "source": {},
    "destination": {}
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
      "connectionId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "delay": {},
      "destination": {},
      "disabledAt": "2026-05-07T12:00:00.000Z",
      "filter": {},
      "folderId": "string",
      "Id": "string",
      "name": "Ava Chen",
      "source": {},
      "status": "string",
      "transformation": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Connection action reference](actions/create-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pabblyHook/latest/actions/create-connection).
