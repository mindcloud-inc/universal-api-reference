# Planyo Universal API Examples

These examples use the MindCloud API key and Planyo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Site Info

Retrieves site information from Planyo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-site-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planyo/latest/actions/get-site-info?${params}`, {
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
      "activeExtensions": [
        {}
      ],
      "adminId": "string",
      "category": "string",
      "customResourceProperties": [
        {}
      ],
      "dateFormat": "string",
      "defaultLanguage": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "onlinePaymentSurcharge": 1,
      "photos": [
        {}
      ],
      "properties": {},
      "timezone": "string",
      "timezoneOffset": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Site Info action reference](actions/get-site-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/planyo/latest/actions/get-site-info).

## Add Reservation Payment

Adds a reservation payment in Planyo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planyo/latest/actions/add-reservation-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reservationId": 1,
  "paymentMode": 1,
  "paymentStatus": 1,
  "transactionId": "string",
  "amount": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planyo/latest/actions/add-reservation-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reservationId": 1,
    "paymentMode": 1,
    "paymentStatus": 1,
    "transactionId": "string",
    "amount": 1,
    "currency": "string"
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
      "paymentId": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Reservation Payment action reference](actions/add-reservation-payment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/planyo/latest/actions/add-reservation-payment).
