# SmartRoutes Universal API Examples

These examples use the MindCloud API key and SmartRoutes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/list-customers?${params}`, {
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
      "account": "string",
      "address": "string",
      "created": "string",
      "duration": 1,
      "email": "ava@example.com",
      "id": 1,
      "lat": 1,
      "lng": 1,
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "postcode": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartRoutes/latest/actions/list-customers).

## Create Vehicle



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/create-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "availability": "0",
  "startLocation": "0",
  "endLocation": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/create-vehicle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "availability": "0",
    "startLocation": "0",
    "endLocation": "0"
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
      "active": true,
      "availability": "string",
      "break": true,
      "capacities": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "endLocation": "string",
      "id": 1,
      "name": "Ava Chen",
      "shift": [
        {}
      ],
      "skills": [
        "string"
      ],
      "startLocation": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Vehicle action reference](actions/create-vehicle.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartRoutes/latest/actions/create-vehicle).
