# timeBuzzer: Update Activity



```
PUT https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "tiles[]": [
    1
  ],
  "startDate": "string",
  "endDate": "string",
  "startUtcOffset": "string",
  "endUtcOffset": "string",
  "billed": true,
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/update-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "tiles[]": [1],
    "startDate": "string",
    "endDate": "string",
    "startUtcOffset": "string",
    "endUtcOffset": "string",
    "billed": true,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The activity ID. |
| `tiles[]` | array<number> | yes | The tile IDs assigned to the activity. Accepts multiple values as an array. |
| `startDate` | string | yes | The activity start timestamp in ISO 8601 format. |
| `endDate` | string | yes | The activity end timestamp in ISO 8601 format. |
| `startUtcOffset` | string | yes | The UTC offset at the start of the activity. |
| `endUtcOffset` | string | yes | The UTC offset at the end of the activity. |
| `note` | string | no | The activity note. |
| `billed` | boolean | yes | Whether the activity is billed. |
| `userId` | number | yes | The user ID that owns the activity. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native timeBuzzer API returns.

## Native endpoint

Through the native timeBuzzer API, this operation is `PUT /open-api/activities/:id` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity.md) for the provider-specific parameters and requirements.

