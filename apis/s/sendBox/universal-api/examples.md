# SendBox Universal API Examples

These examples use the MindCloud API key and SendBox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Saved Addresses



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/list-saved-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/list-saved-addresses?${params}`, {
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
      "count": 1,
      "filter_by": {},
      "page_by": {},
      "query": "string",
      "results": [
        {}
      ],
      "sort_by": [
        {}
      ],
      "view": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Saved Addresses action reference](actions/list-saved-addresses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendBox/latest/actions/list-saved-addresses).

## Create Shipment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel_code": "api",
  "destination": {},
  "incoming_option": "string",
  "items": {},
  "origin": {},
  "package_type": "string",
  "pickup_date": "2026-05-07T12:00:00.000Z",
  "region": "string",
  "service_code": "string",
  "total_value": 1,
  "weight": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel_code": "api",
    "destination": {},
    "incoming_option": "string",
    "items": {},
    "origin": {},
    "package_type": "string",
    "pickup_date": "2026-05-07T12:00:00.000Z",
    "region": "string",
    "service_code": "string",
    "total_value": 1,
    "weight": 1
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
      "amount": 1,
      "code": "string",
      "current_status": {},
      "date_created": "2026-05-07T12:00:00.000Z",
      "destination_city": "string",
      "destination_country": {},
      "destination_name": "Ava Chen",
      "destination_phone": "string",
      "destination_street": "string",
      "fee": 1,
      "has_waybill_error": true,
      "id": "string",
      "items": [
        {}
      ],
      "last_updated": "2026-05-07T12:00:00.000Z",
      "origin_city": "string",
      "origin_name": "Ava Chen",
      "origin_phone": "string",
      "origin_state": {},
      "origin_street": "string",
      "paid": 1,
      "payment_data": {},
      "pickup_courier": {},
      "pickup_date": "2026-05-07T12:00:00.000Z",
      "pk": "string",
      "possible_actions": [
        {}
      ],
      "region": "string",
      "selected_courier_id": "string",
      "status": {},
      "status_code": "string",
      "tracking_code": "string",
      "user_id": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Shipment action reference](actions/create-shipment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendBox/latest/actions/create-shipment).
