# Samedi Universal API Examples

These examples use the MindCloud API key and Samedi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Health Insurances

Retrieves health insurances from Samedi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-health-insurances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-health-insurances?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "type": "string",
      "valid_until": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Health Insurances action reference](actions/list-health-insurances.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/samedi/latest/actions/list-health-insurances).

## Book Appointment

Books an appointment in Samedi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/samedi/latest/actions/book-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventCategoryId": "string",
  "eventTypeId": "string",
  "startsAt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samedi/latest/actions/book-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventCategoryId": "string",
    "eventTypeId": "string",
    "startsAt": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Book Appointment action reference](actions/book-appointment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/samedi/latest/actions/book-appointment).
