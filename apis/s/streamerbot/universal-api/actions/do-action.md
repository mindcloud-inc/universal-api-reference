# Streamer.bot: Do Action

Triggers an existing action in Streamer.bot.

```
POST https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/do-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamer.bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/do-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamerbot/latest/actions/do-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action.id` | string | no | GUID of the Streamer.bot action to execute. Example: `4af4bdef-f396-521f-a1a5-02983ae638cb`. |
| `action.name` | string | no | Name of the Streamer.bot action to execute. Example: `Demo Alert`. |
| `args` | object | no | Optional key-value arguments to pass through to the Streamer.bot action. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Streamer.bot API returns.

## Native endpoint

Through the native Streamer.bot API, this operation is `POST /DoAction` (base URL `https://allow-freely-princess-carefully.trycloudflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/do-action.md) for the provider-specific parameters and requirements.

