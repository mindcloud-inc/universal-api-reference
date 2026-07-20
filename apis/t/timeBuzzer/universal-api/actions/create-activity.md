# timeBuzzer: Create Activity



```
POST https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tiles[]": [
    1
  ],
  "startDate": "string",
  "endDate": "string",
  "startUtcOffset": "string",
  "endUtcOffset": "string",
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tiles[]": [1],
    "startDate": "string",
    "endDate": "string",
    "startUtcOffset": "string",
    "endUtcOffset": "string",
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tiles[]` | array<number> | yes | Tile IDs to associate with the activity. |
| `startDate` | string | yes | Activity start timestamp in ISO 8601 format. |
| `endDate` | string | yes | Activity end timestamp in ISO 8601 format. |
| `startUtcOffset` | string | yes | UTC offset at the activity start time. |
| `endUtcOffset` | string | yes | UTC offset at the activity end time. |
| `note` | string | no | Optional note for the activity. |
| `userId` | number | yes | User ID that owns the activity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billed": true,
      "customData": "string",
      "endDate": "string",
      "endUtcOffset": "string",
      "id": 1,
      "lock_": {},
      "note": "string",
      "startDate": "string",
      "startUtcOffset": "string",
      "tiles": [
        1
      ],
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billed` | boolean | Whether the activity is billed. |
| `customData` | string | Custom activity data when present. |
| `endDate` | string | Activity end timestamp in ISO 8601 format. |
| `endUtcOffset` | string | UTC offset at the activity end. |
| `id` | number | Activity ID. |
| `lock_` | object | Lock-state metadata returned by timeBuzzer. |
| `note` | string | Activity note text. |
| `startDate` | string | Activity start timestamp in ISO 8601 format. |
| `startUtcOffset` | string | UTC offset at the activity start. |
| `tiles` | array<number> | Tile IDs assigned to the activity. |
| `userId` | number | Owning user ID. |

## Native endpoint

Through the native timeBuzzer API, this operation is `POST /open-api/activities` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

