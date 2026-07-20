# Shippify Universal API Examples

These examples use the MindCloud API key and Shippify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Countries

Retrieves the list of supported countries from Shippify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippify/latest/actions/list-countries?${params}`, {
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
      "countryCode": "string",
      "createdAt": "string",
      "defaultCityId": 1,
      "defaultCityName": "Ava Chen",
      "id": 1,
      "isSaasVisible": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Countries action reference](actions/list-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shippify/latest/actions/list-countries).

## Add Deliveries To Route

Adds deliveries to an existing route in Shippify.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/add-deliveries-to-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "routeId": "string",
  "deliveries[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippify/latest/actions/add-deliveries-to-route', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "routeId": "string",
    "deliveries[]": ["string"]
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
      "code": "string",
      "data": {
        "jobs": [
          [
            {}
          ]
        ]
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Deliveries To Route action reference](actions/add-deliveries-to-route.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shippify/latest/actions/add-deliveries-to-route).
