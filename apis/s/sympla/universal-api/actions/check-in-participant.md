# Sympla: Check In Participant

Checks in a participant in Sympla by participant ID.

```
PUT https://connect.mindcloud.co/v1/universal/sympla/latest/actions/check-in-participant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sympla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sympla/latest/actions/check-in-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "participantId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sympla/latest/actions/check-in-participant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "participantId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | Unique identifier of the event. |
| `participantId` | number | yes | Unique identifier of the participant ticket to check in. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Sympla API, this operation is `POST /events/:eventId/participants/:participantId/checkin` (base URL `https://api.sympla.com.br/public/v1.5.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-in-participant.md) for the provider-specific parameters and requirements.

