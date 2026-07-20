# Zeo Route Planner Universal API Examples

These examples use the MindCloud API key and Zeo Route Planner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Drivers

Retrieves drivers from Zeo Route Planner.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-drivers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-drivers?${params}`, {
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
      "address": "string",
      "countryCodeName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "phoneNo": "string",
      "postalCode": "string",
      "vehicleType": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Drivers action reference](actions/list-drivers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zeoRoutePlanner/latest/actions/list-drivers).

## Create Driver

Creates a new driver in Zeo Route Planner.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-driver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-driver', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "address": "string",
      "countryCodeName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "phoneNo": "string",
      "postalCode": "string",
      "vehicleType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Driver action reference](actions/create-driver.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zeoRoutePlanner/latest/actions/create-driver).
