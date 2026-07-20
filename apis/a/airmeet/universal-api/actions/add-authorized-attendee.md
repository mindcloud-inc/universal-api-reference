# Airmeet: Add Authorized Attendee

Creates an authorized attendee in Airmeet.

```
POST https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/add-authorized-attendee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/add-authorized-attendee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "airmeetId": "string",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/add-authorized-attendee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "airmeetId": "string",
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `airmeetId` | string | yes | The Airmeet event ID. |
| `attendanceType` | string | no | Required for hybrid events. Use IN-PERSON or VIRTUAL. |
| `email` | string | yes | The attendee email address. |
| `firstName` | string | yes | The attendee first name. |
| `lastName` | string | yes | The attendee last name. |
| `registerAttendee` | boolean | no | Set true to confirm the registration immediately instead of leaving it pending. |
| `sendEmailInvite` | boolean | no | Set false to skip sending the attendee email invite. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `POST /airmeet/{airmeetId}/attendee` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-authorized-attendee.md) for the provider-specific parameters and requirements.

