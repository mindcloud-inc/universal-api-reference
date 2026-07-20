# Trafft Universal API Examples

These examples use the MindCloud API key and Trafft connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Customers

Retrieves customers from Trafft.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-customers?${params}`, {
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
      "data": {
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "phone_country_code": "string",
        "phone_number": "string"
      },
      "pagination": {
        "limit": 1,
        "page": 1,
        "pages": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [List Customers action reference](actions/list-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trafft/latest/actions/list-customers).

## Create Booking

Creates a new booking in Trafft.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service": 1,
  "employee": 1,
  "date": "string",
  "time": "string",
  "customer": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trafft/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service": 1,
    "employee": 1,
    "date": "string",
    "time": "string",
    "customer": 1
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Booking action reference](actions/create-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trafft/latest/actions/create-booking).
