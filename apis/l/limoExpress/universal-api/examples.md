# LimoExpress Universal API Examples

These examples use the MindCloud API key and LimoExpress connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Booking Statuses

Retrieves booking statuses from the LimoExpress organization.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-booking-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-booking-statuses?${params}`, {
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
      "code": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Booking Statuses action reference](actions/list-booking-statuses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/limoExpress/latest/actions/list-booking-statuses).

## Add Currency

Adds a currency to the LimoExpress organization.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/add-currency" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currencyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/add-currency', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currencyId": "string"
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
      "data": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Currency action reference](actions/add-currency.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/limoExpress/latest/actions/add-currency).
