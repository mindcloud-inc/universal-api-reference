# Placker: Create Card On List



```
POST https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-card-on-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-card-on-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list": "1235",
  "title": "Task 123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placker/latest/actions/create-card-on-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list": "1235",
    "title": "Task 123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list` | number | yes | List ID. Example: `1235`. |
| `title` | string | yes | Card title. Example: `Task 123`. |
| `description` | string | no | Card description. Example: `This is a task description`. |
| `status` | string | no | Card status. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Example: `OPEN`. |
| `startDates.planned` | date | no | Planned start date. Example: `2020-07-21T17:32:28+02:00`. |
| `startDates.actual` | date | no | Actual start date. Example: `2020-07-21T17:32:28+02:00`. |
| `endDates.planned` | date | no | Planned end date. Example: `2020-08-21T17:32:28+02:00`. |
| `endDates.actual` | date | no | Actual end date. Example: `2020-08-21T17:32:28+02:00`. |
| `order` | number | no | Card order within the list. Example: `1000.5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Placker API returns.

## Native endpoint

Through the native Placker API, this operation is `POST /list/:list/card` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-card-on-list.md) for the provider-specific parameters and requirements.

