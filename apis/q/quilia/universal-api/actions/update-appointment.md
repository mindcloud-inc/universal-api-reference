# Quilia: Update Appointment



```
PUT https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quilia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quilia/latest/actions/update-appointment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caseId` | string | no | The case ID to associate with the appointment |
| `contactId` | string | no | The contact/people ID to associate with the appointment |
| `id` | string | yes | The unique identifier of the appointment to update |
| `notes` | string | no | Additional notes or details about the appointment |
| `userId` | string | no | The user ID to assign the appointment to |
| `start` | date | no | ISO timestamp for the appointment start time |
| `end` | date | no | ISO timestamp for the appointment end time |
| `status` | list<string> | no | The status of the appointment One of: `cancelled`, `confirmed`, `released`, `rescheduled`, `scheduled`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Quilia API returns.

## Native endpoint

Through the native Quilia API, this operation is `PATCH appointments/:id` (base URL `https://api.quilia.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-appointment.md) for the provider-specific parameters and requirements.

