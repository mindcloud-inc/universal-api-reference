# GoodDay.work: Create Event

Creates a new event in GoodDay.work.

```
POST https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "createdByUserId": "string",
  "eventType": "string",
  "name": "Ava Chen",
  "startDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "createdByUserId": "string",
    "eventType": "string",
    "name": "Ava Chen",
    "startDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdByUserId` | string | yes | User ID on whose behalf the event is created. |
| `eventType` | string | yes | GoodDay event type. |
| `name` | string | yes | Event name. |
| `startDate` | string | yes | Event start date in YYYY-MM-DD. |
| `endDate` | string | no | Event end date in YYYY-MM-DD. |
| `projectId` | string | no | Project ID for project events. |
| `userId` | string | no | User ID for personal events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": "string",
      "createdByUserId": "string",
      "endDate": "string",
      "eventType": "string",
      "id": "string",
      "momentCreated": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "startDate": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | string | Assigned user ID, if any. |
| `createdByUserId` | string | User who created the event. |
| `endDate` | string | Event end date. |
| `eventType` | string | Event type. |
| `id` | string | Created event ID. |
| `momentCreated` | string | Creation timestamp. |
| `name` | string | Event name. |
| `projectId` | string | Associated project ID. |
| `startDate` | string | Event start date. |
| `userId` | string | Associated user ID, if any. |

## Native endpoint

Through the native GoodDay.work API, this operation is `POST /events` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

