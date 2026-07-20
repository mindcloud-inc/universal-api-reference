# Cerbo Universal API Examples

These examples use the MindCloud API key and Cerbo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves user records from Cerbo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-users?${params}`, {
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
      "active": true,
      "created": "string",
      "displayNameForAppointments": "Ava Chen",
      "displayNameForMessages": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasCalendar": true,
      "id": "string",
      "isResource": true,
      "lastName": "Chen",
      "loginActive": true,
      "middleName": "Ava Chen",
      "npi": "string",
      "object": "string",
      "prefix": "string",
      "suffix": "string",
      "userNotes": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cerbo/latest/actions/list-users).

## Add Patient Health Maintenance Reading

Adds a patient health maintenance reading in Cerbo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/add-patient-health-maintenance-reading" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "patient_id": 1,
  "health_maintenance_id": 1,
  "date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/add-patient-health-maintenance-reading', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "patient_id": 1,
    "health_maintenance_id": 1,
    "date": "string"
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

See the full [Add Patient Health Maintenance Reading action reference](actions/add-patient-health-maintenance-reading.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cerbo/latest/actions/add-patient-health-maintenance-reading).
