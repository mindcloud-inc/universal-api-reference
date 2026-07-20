# MoneyBird Universal API Examples

These examples use the MindCloud API key and MoneyBird connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Administrations

Retrieves administrations from MoneyBird.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-administrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/list-administrations?${params}`, {
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
      "access": "string",
      "country": "string",
      "currency": "string",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "period_locked_until": "string",
      "period_start_date": "2026-05-07T12:00:00.000Z",
      "suspended": true,
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Administrations action reference](actions/list-administrations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moneyBird/latest/actions/list-administrations).

## Create Contact

Creates a new contact in MoneyBird.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "administrationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "administrationId": "string"
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
      "administrationId": "string",
      "archived": true,
      "city": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "lastname": "Chen",
      "phone": "string",
      "taxNumber": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moneyBird/latest/actions/create-contact).
