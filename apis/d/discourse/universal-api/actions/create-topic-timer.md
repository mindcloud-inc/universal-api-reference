# Discourse: Create Topic Timer

Creates a topic timer in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-topic-timer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-topic-timer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "time": "string",
  "status_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-topic-timer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "time": "string",
    "status_type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `based_on_last_post` | boolean | no | Whether the timer should be based on the last post. |
| `category_id` | number | no | Optional category id used by the timer action. |
| `id` | number | yes | Topic id. |
| `time` | string | yes | Execution time for the topic timer. |
| `status_type` | string | yes | Topic timer status type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "based_on_last_post": true,
      "category_id": 1,
      "closed": true,
      "duration_minutes": "string",
      "execute_at": "string",
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `based_on_last_post` | boolean |  |
| `category_id` | number |  |
| `closed` | boolean |  |
| `duration_minutes` | string |  |
| `execute_at` | string |  |
| `success` | string |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /t/:id/timer.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-topic-timer.md) for the provider-specific parameters and requirements.

