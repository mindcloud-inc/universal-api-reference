# ECAL: Create Private Event

Creates a private event for an ECAL subscriber.

```
POST https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/create-private-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/create-private-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ecalId": "string",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/create-private-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ecalId": "string",
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ecalId` | string | yes | Subscriber ecal_id value that receives the private event. |
| `requestBody` | object | yes | JSON object matching ECAL's private event creation payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarId": "string",
      "description": "string",
      "ecalId": "string",
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
| `ecalId` | string |  |
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

Through the native ECAL API, this operation is `POST /event/` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-private-event.md) for the provider-specific parameters and requirements.

