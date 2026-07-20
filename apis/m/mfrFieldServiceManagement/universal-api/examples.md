# mfr Field Service Management Universal API Examples

These examples use the MindCloud API key and mfr Field Service Management connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Service Requests

Retrieves service requests from mfr Field Service Management.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-service-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/list-service-requests?${params}`, {
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
      "closedAt": "string",
      "costCenterId": "string",
      "createFromServiceRequestTemplateId": "string",
      "currentOwnerId": 1,
      "customerId": 1,
      "customValues": [
        {}
      ],
      "dateModified": "2026-05-07T12:00:00.000Z",
      "dateOfCreation": "string",
      "description": "string",
      "externalId": "string",
      "id": 1,
      "isTemplate": true,
      "isTemplateMobile": true,
      "location": {},
      "name": "Ava Chen",
      "parentServiceRequestId": "string",
      "portalLink": "https://example.com",
      "releasedAt": "string",
      "state": "string",
      "targetTimeInMinutes": "string",
      "type": "string",
      "version": 1,
      "workDoneAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Service Requests action reference](actions/list-service-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mfrFieldServiceManagement/latest/actions/list-service-requests).

## Create Appointment

Creates an appointment in mfr Field Service Management.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "state": "string",
  "startDateTime": "2026-05-07T12:00:00.000Z",
  "endDateTime": "2026-05-07T12:00:00.000Z",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mfrFieldServiceManagement/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "state": "string",
    "startDateTime": "2026-05-07T12:00:00.000Z",
    "endDateTime": "2026-05-07T12:00:00.000Z",
    "contactId": "string"
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
      "appointmentType": "string",
      "contactId": 1,
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "serviceRequestId": 1,
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Appointment action reference](actions/create-appointment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mfrFieldServiceManagement/latest/actions/create-appointment).
