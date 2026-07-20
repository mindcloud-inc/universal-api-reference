# RO App Universal API Examples

These examples use the MindCloud API key and RO App connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/get-company?${params}`, {
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
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "currency_symbol": "string",
      "email": "ava@example.com",
      "logo": "string",
      "name": "Ava Chen",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company action reference](actions/get-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rOApp/latest/actions/get-company).

## Create Booking



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branchId": 1,
  "assigneeId": 1,
  "clientId": 1,
  "scheduledFor": "2026-05-07T12:00:00.000Z",
  "scheduledTo": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branchId": 1,
    "assigneeId": 1,
    "clientId": 1,
    "scheduledFor": "2026-05-07T12:00:00.000Z",
    "scheduledTo": "2026-05-07T12:00:00.000Z"
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
      "assignee_id": 1,
      "branch_id": 1,
      "client_id": 1,
      "comment": "string",
      "resource_id": 1,
      "scheduled_for": "2026-05-07T12:00:00.000Z",
      "scheduled_to": "2026-05-07T12:00:00.000Z",
      "status_id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Booking action reference](actions/create-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rOApp/latest/actions/create-booking).
