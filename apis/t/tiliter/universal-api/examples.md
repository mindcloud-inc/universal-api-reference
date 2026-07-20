# Tiliter Universal API Examples

These examples use the MindCloud API key and Tiliter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Health Check

Retrieves the Tiliter Recognition API health status.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/health-check?${params}`, {
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
      "authenticatedCustomerId": {
        "dependency": {},
        "useCache": true
      },
      "it's": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Health Check action reference](actions/health-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tiliter/latest/actions/health-check).

## Create Device

Creates a device in the Tiliter Recognition API.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-device" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceIdPath": "string",
  "deviceId": "string",
  "cameras[]": [
    "string"
  ],
  "operationalMode": "string",
  "storeId": "string",
  "departments[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-device', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceIdPath": "string",
    "deviceId": "string",
    "cameras[]": ["string"],
    "cameras[]": ["string"],
    "operationalMode": "string",
    "storeId": "string",
    "departments[]": ["string"],
    "departments[]": ["string"]
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
      "cameras": [
        "string"
      ],
      "departments": [
        "string"
      ],
      "deviceId": "string",
      "operationalMode": "string",
      "storeId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Device action reference](actions/create-device.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tiliter/latest/actions/create-device).
