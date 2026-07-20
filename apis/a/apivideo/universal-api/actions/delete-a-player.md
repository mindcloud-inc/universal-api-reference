# api.video: Delete a player

Deletes a player theme from api.video.

```
DELETE https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/delete-a-player
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api.video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/delete-a-player?connectionId=$CONNECTION_ID&playerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "playerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/delete-a-player?${params}`, {
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
| `playerId` | string | yes | The unique identifier for the player theme. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native api.video API returns.

## Native endpoint

Through the native api.video API, this operation is `DELETE /players/:playerId` (base URL `https://ws.api.video`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-player.md) for the provider-specific parameters and requirements.

