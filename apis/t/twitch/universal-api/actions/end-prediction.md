# Twitch: End Prediction

Ends an existing prediction in Twitch.

```
PUT https://connect.mindcloud.co/v1/universal/twitch/latest/actions/end-prediction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/end-prediction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasterId": "string",
  "id": "string",
  "status": "CANCELED"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twitch/latest/actions/end-prediction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasterId": "string",
    "id": "string",
    "status": "CANCELED"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcasterId` | string | yes | The ID of the broadcaster that’s running the prediction. |
| `id` | string | yes | The ID of the prediction to update. |
| `status` | string | yes | The status to set the prediction to. One of: `CANCELED`, `LOCKED`, `RESOLVED`. |
| `winningOutcomeId` | string | no | The ID of the winning outcome when resolving a prediction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "broadcasterId": "string",
          "broadcasterLogin": "string",
          "broadcasterName": "Ava Chen",
          "createdAt": "string",
          "endedAt": "string",
          "id": "string",
          "lockedAt": "string",
          "outcomes": [
            {
              "channelPoints": 1,
              "color": "string",
              "id": "string",
              "title": "string",
              "topPredictors": [
                {
                  "channelPointsUsed": 1,
                  "channelPointsWon": 1,
                  "userId": "string",
                  "userLogin": "string",
                  "userName": "Ava Chen"
                }
              ],
              "users": 1
            }
          ],
          "predictionWindow": 1,
          "status": "string",
          "title": "string",
          "winningOutcomeId": "string"
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
| `data` | array<object> | Prediction rows. |
| `data[].broadcasterId` | string | Broadcaster identifier. |
| `data[].broadcasterLogin` | string | Broadcaster login name. |
| `data[].broadcasterName` | string | Broadcaster display name. |
| `data[].createdAt` | string | Timestamp when the prediction started. |
| `data[].endedAt` | string | Timestamp when the prediction ended. |
| `data[].id` | string | Prediction identifier. |
| `data[].lockedAt` | string | Timestamp when the prediction was locked. |
| `data[].outcomes` | array<object> | Prediction outcome rows. |
| `data[].outcomes[].channelPoints` | number | Channel points spent on the outcome. |
| `data[].outcomes[].color` | string | Outcome display color. |
| `data[].outcomes[].id` | string | Outcome identifier. |
| `data[].outcomes[].title` | string | Outcome title. |
| `data[].outcomes[].topPredictors` | array<object> | Top predictor rows when present. |
| `data[].outcomes[].topPredictors[].channelPointsUsed` | number | Channel points used by the predictor. |
| `data[].outcomes[].topPredictors[].channelPointsWon` | number | Channel points won by the predictor. |
| `data[].outcomes[].topPredictors[].userId` | string | Top predictor user identifier. |
| `data[].outcomes[].topPredictors[].userLogin` | string | Top predictor login name. |
| `data[].outcomes[].topPredictors[].userName` | string | Top predictor display name. |
| `data[].outcomes[].users` | number | Number of users who chose the outcome. |
| `data[].predictionWindow` | number | Prediction window in seconds. |
| `data[].status` | string | Prediction status. |
| `data[].title` | string | Prediction title. |
| `data[].winningOutcomeId` | string | Winning outcome identifier when resolved. |

## Native endpoint

Through the native Twitch API, this operation is `PATCH /predictions` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/end-prediction.md) for the provider-specific parameters and requirements.

