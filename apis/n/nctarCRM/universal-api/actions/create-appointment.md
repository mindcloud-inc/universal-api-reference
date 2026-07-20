# Néctar CRM: Create Appointment

Creates a new appointment in Néctar CRM.

```
POST https://connect.mindcloud.co/v1/universal/nctarCRM/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Néctar CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nctarCRM/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "client": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nctarCRM/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "startDate": "2026-05-07T12:00:00.000Z",
    "endDate": "2026-05-07T12:00:00.000Z",
    "client": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Appointment subject. |
| `startDate` | date | yes | Appointment start datetime. |
| `endDate` | date | yes | Appointment end datetime. |
| `client` | object | yes | Contact object for the appointment, for example {"id": 2}. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Néctar CRM API returns.

## Native endpoint

Through the native Néctar CRM API, this operation is `POST /compromissos/` (base URL `https://app.nectarcrm.com.br/crm/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

