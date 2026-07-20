# Ship24 Universal API Examples

These examples use the MindCloud API key and Ship24 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Couriers

Retrieves all available couriers from Ship24.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-couriers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ship24/latest/actions/list-couriers?${params}`, {
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
      "countryCode": {},
      "courierCode": "string",
      "courierName": "Ava Chen",
      "isDeprecated": true,
      "isPost": true,
      "requiredFields": {},
      "website": {}
    }
  ],
  "meta": {}
}
```

See the full [List Couriers action reference](actions/list-couriers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ship24/latest/actions/list-couriers).

## Bulk Create Trackers

Creates multiple new trackers in Ship24.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/bulk-create-trackers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ship24/latest/actions/bulk-create-trackers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackers[]": [{}]
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
      "errors": [
        {}
      ],
      "inputData": {},
      "itemStatus": "string",
      "tracker": {}
    }
  ],
  "meta": {}
}
```

See the full [Bulk Create Trackers action reference](actions/bulk-create-trackers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ship24/latest/actions/bulk-create-trackers).
