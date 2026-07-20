# GoodDay.work: List Events

Finds events in the GoodDay.work workspace.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-events?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-events?${params}`, {
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
| `startDate` | string | yes | Events start date in YYYY-MM-DD. |
| `endDate` | string | yes | Events end date in YYYY-MM-DD. |
| `eventTypes` | string | no | Comma-separated GoodDay event types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "eventType": "string",
      "id": "string",
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
| `endDate` | string | Event end date. |
| `eventType` | string | Event type. |
| `id` | string | Event ID. |
| `name` | string | Event name. |
| `projectId` | string | Associated project ID. |
| `startDate` | string | Event start date. |
| `userId` | string | Associated user ID. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /events` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

