# Hub Planner: Get Booking

Retrieves a booking from Hub Planner.

```
GET https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hub Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-booking?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-booking?${params}`, {
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
| `id` | string | yes | Hub Planner booking ID from the _id field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "allDay": true,
      "categoryName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "end": "2026-05-07T12:00:00.000Z",
      "metadata": "string",
      "project": "string",
      "resource": "string",
      "scale": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "stateValue": 1,
      "title": "string",
      "type": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `allDay` | boolean |  |
| `categoryName` | string |  |
| `createdDate` | date |  |
| `end` | date |  |
| `metadata` | string |  |
| `project` | string |  |
| `resource` | string |  |
| `scale` | string |  |
| `start` | date |  |
| `state` | string |  |
| `stateValue` | number |  |
| `title` | string |  |
| `type` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Hub Planner API, this operation is `GET /booking/:id` (base URL `https://api.hubplanner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking.md) for the provider-specific parameters and requirements.

