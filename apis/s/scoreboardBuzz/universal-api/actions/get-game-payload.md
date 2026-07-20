# Scoreboard Buzz: Get Game Payload

Retrieves a game payload from Scoreboard Buzz.

```
GET https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/get-game-payload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoreboard Buzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/get-game-payload?connectionId=$CONNECTION_ID&gameId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "gameId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/get-game-payload?${params}`, {
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
| `gameId` | string | yes | Game ID or managed game ID. |
| `date` | date | no | Historical date to view in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accounts": [
          {
            "account_id": 1,
            "name": "Ava Chen",
            "timezone": "string"
          }
        ],
        "members": [
          {
            "account_id": 1,
            "extra_info": {
              "user_ids": [
                1
              ]
            },
            "id": 1,
            "name": "Ava Chen"
          }
        ],
        "settings": {
          "account_id": 1,
          "end_date": "2026-05-07T12:00:00.000Z",
          "end_hour": 1,
          "end_minute": 1,
          "frequency": 1,
          "game_mode": 1,
          "game_type": 1,
          "id": 1,
          "is_managed_game": true,
          "member_type": 1,
          "name": "Ava Chen",
          "start_date": "2026-05-07T12:00:00.000Z",
          "start_hour": 1,
          "start_minute": 1
        },
        "trackables": [
          {
            "activity": [
              {
                "account_id": 1,
                "member_id": 1,
                "total_amount": 1,
                "total_value": 1
              }
            ],
            "game_product_id": 1,
            "goal": 1,
            "info": [
              {
                "account_id": 1,
                "id": 1,
                "name": "Ava Chen"
              }
            ],
            "order": 1,
            "trackable_mode": 1
          }
        ]
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Rendered game payload. |
| `data.accounts` | array<object> | Accounts participating in the game. |
| `data.accounts[].account_id` | number | Account ID. |
| `data.accounts[].name` | string | Account name. |
| `data.accounts[].timezone` | string | Account timezone. |
| `data.members` | array<object> | Members included in the game. |
| `data.members[].account_id` | number | Member account ID. |
| `data.members[].extra_info` | object | Additional member metadata returned by the provider. |
| `data.members[].extra_info.user_ids` | array<number> | Provider user IDs associated with the member. |
| `data.members[].id` | number | Member ID. |
| `data.members[].name` | string | Member name. |
| `data.settings` | object | Game settings for the requested period. |
| `data.settings.account_id` | number | Account ID. |
| `data.settings.end_date` | date | Period end date. |
| `data.settings.end_hour` | number | UTC hour when the scoring period ends. |
| `data.settings.end_minute` | number | Minute within the ending hour when the scoring period ends. |
| `data.settings.frequency` | number | Game frequency code. |
| `data.settings.game_mode` | number | Game mode code. |
| `data.settings.game_type` | number | Game type code. |
| `data.settings.id` | number | Game ID. |
| `data.settings.is_managed_game` | boolean | Whether the game is managed by the provider. |
| `data.settings.member_type` | number | Member type code. |
| `data.settings.name` | string | Game name. |
| `data.settings.start_date` | date | Period start date. |
| `data.settings.start_hour` | number | UTC hour when the scoring period starts. |
| `data.settings.start_minute` | number | Minute within the starting hour when the scoring period starts. |
| `data.trackables` | array<object> | Trackables attached to the game. |
| `data.trackables[].activity` | array<object> | Aggregated activity totals for the trackable. |
| `data.trackables[].activity[].account_id` | number | Account ID for the aggregate row. |
| `data.trackables[].activity[].member_id` | number | Member ID for the aggregate row. |
| `data.trackables[].activity[].total_amount` | number | Total quantity scored. |
| `data.trackables[].activity[].total_value` | number | Total value scored. |
| `data.trackables[].game_product_id` | number | Game-product link ID. |
| `data.trackables[].goal` | number | Goal value. |
| `data.trackables[].info` | array<object> | Trackable metadata. |
| `data.trackables[].info[].account_id` | number | Trackable account ID. |
| `data.trackables[].info[].id` | number | Trackable ID. |
| `data.trackables[].info[].name` | string | Trackable name. |
| `data.trackables[].order` | number | Trackable order. |
| `data.trackables[].trackable_mode` | number | Trackable mode code. |
| `success` | boolean | Whether the payload request succeeded. |

## Native endpoint

Through the native Scoreboard Buzz API, this operation is `GET /games/:gameId/payload` (base URL `https://api.scoreboardbuzz.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-game-payload.md) for the provider-specific parameters and requirements.

