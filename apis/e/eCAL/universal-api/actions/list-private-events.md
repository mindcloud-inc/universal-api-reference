# ECAL: List Private Events

Retrieves a subscriber's private events from ECAL.

```
GET https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-private-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-private-events?connectionId=$CONNECTION_ID&limit=25&offset=0&ecalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "ecalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-private-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ecalId` | string | yes | Subscriber ecal_id value for private events. |

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

Through the native ECAL API, this operation is `GET /event/` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-private-events.md) for the provider-specific parameters and requirements.

