# Twitch: List Predictions

Retrieves broadcaster prediction records from Twitch.

```
GET https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-predictions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twitch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-predictions?connectionId=$CONNECTION_ID&broadcasterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "broadcasterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twitch/latest/actions/list-predictions?${params}`, {
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
| `broadcasterId` | string | yes | ID of the broadcaster whose predictions you want to read. Must match the user in the OAuth token. |
| `id` | string | no | Optional prediction ID filter. Twitch accepts up to 25 IDs. Accepts multiple values as an array. |

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
      ],
      "pagination": {
        "cursor": "string"
      }
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
| `pagination` | object | Pagination cursor payload. |
| `pagination.cursor` | string | Cursor for the next page of results. |

## Native endpoint

Through the native Twitch API, this operation is `GET /predictions` (base URL `https://api.twitch.tv/helix`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-predictions.md) for the provider-specific parameters and requirements.

