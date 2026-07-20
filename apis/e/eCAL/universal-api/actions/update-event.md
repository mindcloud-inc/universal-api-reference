# ECAL: Update Event

Updates an ECAL event by ID or reference.

```
PUT https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventIdOrReference": "string",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventIdOrReference": "string",
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventIdOrReference` | string | yes | ECAL event ID or reference accepted by the update endpoint. |
| `requestBody` | object | yes | JSON object matching ECAL's update event payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarId": "string",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "location": "string",
      "name": "Ava Chen",
      "reference": "string",
      "referenceType": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timezone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarId` | string |  |
| `description` | string |  |
| `endDate` | date |  |
| `id` | string |  |
| `location` | string |  |
| `name` | string |  |
| `reference` | string |  |
| `referenceType` | string |  |
| `startDate` | date |  |
| `status` | string |  |
| `timezone` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ECAL API, this operation is `PUT /event/:eventIdOrReference` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

