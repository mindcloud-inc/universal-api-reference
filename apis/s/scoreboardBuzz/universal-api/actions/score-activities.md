# Scoreboard Buzz: Score Activities

Creates scored activities in Scoreboard Buzz in one request.

```
POST https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/score-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoreboard Buzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/score-activities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input[]": [
    {}
  ],
  "input[].userId": 1,
  "input[].trackableId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/score-activities', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input[]": [{}],
    "input[].userId": 1,
    "input[].trackableId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input[]` | array<object> | yes | Array of activities to score in one request. |
| `input[].userId` | number | yes | ID of the user to score the activity for. |
| `input[].trackableId` | number | yes | ID of the trackable to score. |
| `input[].productName` | string | no | Optional product name for reference only. |
| `input[].quantity` | number | no | Number of units to score. Defaults to 1. Default: `1`. |
| `input[].value` | number | no | Value amount to score. Defaults to 0. Default: `0`. |
| `input[].memo` | string | no | Optional memo text for the activity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        {
          "amount": 1,
          "created": "2026-05-07T12:00:00.000Z",
          "deactivated": true,
          "id": 1,
          "memo": "string",
          "modified": "2026-05-07T12:00:00.000Z",
          "product_id": 1,
          "user_id": 1,
          "value": 1
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | array<object> | Activities created by the request. |
| `activities[].amount` | number | Quantity scored. |
| `activities[].created` | date | Creation timestamp. |
| `activities[].deactivated` | boolean | Whether the activity has been deactivated. |
| `activities[].id` | number | Created activity ID. |
| `activities[].memo` | string | Memo saved on the activity. |
| `activities[].modified` | date | Last modification timestamp. |
| `activities[].product_id` | number | Trackable ID stored as product_id. |
| `activities[].user_id` | number | User ID for the created activity. |
| `activities[].value` | number | Value amount scored. |
| `success` | boolean | Whether the activities were scored successfully. |

## Native endpoint

Through the native Scoreboard Buzz API, this operation is `POST /activities` (base URL `https://api.scoreboardbuzz.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/score-activities.md) for the provider-specific parameters and requirements.

