# Bookingmood Universal API Examples

These examples use the MindCloud API key and Bookingmood connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves product records from the Bookingmood API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-products?${params}`, {
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
      "ac_id": "string",
      "approximate_address": "string",
      "approximate_coordinates": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": {},
      "fee": {},
      "id": "string",
      "images": [
        {}
      ],
      "interaction": "string",
      "name": {},
      "organization_id": "string",
      "rent_period": "string",
      "request_status": "string",
      "services": [
        {}
      ],
      "timezone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bookingmood/latest/actions/list-products).

## Book

Creates a booking in Bookingmood from product, interval, occupancy, and form values.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/book" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "interval.end": "string",
  "interval.start": "string",
  "occupancy": "string",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/book', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "interval.end": "string",
    "interval.start": "string",
    "occupancy": "string",
    "productId": "string"
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
      "booking_id": "string",
      "payment_url": "https://example.com",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

See the full [Book action reference](actions/book.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bookingmood/latest/actions/book).
