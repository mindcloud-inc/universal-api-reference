# Queue Times: Get Park Queue Times



```
GET https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/get-park-queue-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue Times `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/get-park-queue-times?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queueTimes/latest/actions/get-park-queue-times?${params}`, {
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
| `id` | number | yes | Numeric park ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lands": [
        {
          "id": 1,
          "name": "Ava Chen",
          "rides": [
            {
              "id": 1,
              "is_open": true,
              "last_updated": "string",
              "name": "Ava Chen",
              "wait_time": 1
            }
          ]
        }
      ],
      "rides": [
        {
          "id": 1,
          "is_open": true,
          "last_updated": "string",
          "name": "Ava Chen",
          "wait_time": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lands` | array<object> |  |
| `lands[].id` | number |  |
| `lands[].name` | string |  |
| `lands[].rides` | array<object> |  |
| `lands[].rides[].id` | number |  |
| `lands[].rides[].is_open` | boolean |  |
| `lands[].rides[].last_updated` | string |  |
| `lands[].rides[].name` | string |  |
| `lands[].rides[].wait_time` | number |  |
| `rides` | array<object> |  |
| `rides[].id` | number |  |
| `rides[].is_open` | boolean |  |
| `rides[].last_updated` | string |  |
| `rides[].name` | string |  |
| `rides[].wait_time` | number |  |

## Native endpoint

Through the native Queue Times API, this operation is `GET /parks/:id/queue_times.json` (base URL `https://queue-times.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-park-queue-times.md) for the provider-specific parameters and requirements.

