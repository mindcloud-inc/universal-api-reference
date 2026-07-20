# GoodDay.work: Get Event

Retrieves a single event from GoodDay.work.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=w8JXld" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "w8JXld"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | GoodDay event ID. Default: `w8JXld`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": "string",
      "endDate": "string",
      "eventType": "string",
      "id": "string",
      "isAccomplished": true,
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
| `endDate` | string | Event end date. |
| `eventType` | string | Event type. |
| `id` | string | Event ID. |
| `isAccomplished` | boolean | Whether the event is marked accomplished. |
| `momentCreated` | string | Creation timestamp. |
| `name` | string | Event name. |
| `projectId` | string | Associated project ID. |
| `startDate` | string | Event start date. |
| `userId` | string | Associated user ID, if any. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /event/:eventId` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

