# api.video: Update a player

Updates an existing player theme in api.video.

```
PUT https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/update-a-player
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api.video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/update-a-player" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "playerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/update-a-player', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "playerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Optional updated display name for the player theme. |
| `playerId` | string | yes | The unique identifier for the player theme. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native api.video API returns.

## Native endpoint

Through the native api.video API, this operation is `PATCH /players/:playerId` (base URL `https://ws.api.video`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-player.md) for the provider-specific parameters and requirements.

