# Rubitime Universal API Examples

These examples use the MindCloud API key and Rubitime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Record

Retrieves a record from Rubitime.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-record?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/get-record?${params}`, {
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
      "comment": "string",
      "duration": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "price": 1,
      "record": "string",
      "status": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Record action reference](actions/get-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rubitime/latest/actions/get-record).

## Create Record

Creates a new record in Rubitime.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branchId": 1,
  "cooperatorId": 1,
  "serviceId": 1,
  "record": "2026-05-01 10:00:00",
  "status": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branchId": 1,
    "cooperatorId": 1,
    "serviceId": 1,
    "record": "2026-05-01 10:00:00",
    "status": "0"
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
      "id": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Record action reference](actions/create-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rubitime/latest/actions/create-record).
