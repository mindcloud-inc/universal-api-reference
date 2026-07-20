# Resource Guru Universal API Examples

These examples use the MindCloud API key and Resource Guru connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Resources

Retrieves resources from Resource Guru.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/list-resources?${params}`, {
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
      "booking_approver_ids": [
        1
      ],
      "color": "string",
      "created_at": "string",
      "creator_id": 1,
      "first_name": "Ava",
      "historical_timezones": [
        {}
      ],
      "id": 1,
      "last_name": "Chen",
      "last_updated_by": "string",
      "name": "Ava Chen",
      "rate_id": 1,
      "resource_type": {},
      "should_submit_timesheets_from": "string",
      "timesheet_approver_ids": [
        1
      ],
      "timezone": {},
      "type": "string",
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Resources action reference](actions/list-resources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/resourceGuru/latest/actions/list-resources).

## Create Booking

Creates a new booking in Resource Guru.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/create-booking', {
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
      "end_at": "string",
      "id": 1,
      "project_id": 1,
      "resource_id": 1,
      "start_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Booking action reference](actions/create-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/resourceGuru/latest/actions/create-booking).
