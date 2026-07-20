# MessageBird: Create Navigator



```
POST https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-navigator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-navigator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/create-navigator', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | The Bird workspace ID where the navigator should be created. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "navigatorId": "string",
      "settings": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `name` | string | The name of the navigator. |
| `navigatorId` | string | The unique identifier of the navigator. |
| `settings` | string |  |
| `type` | string | The type of navigator defines how the navigator selects a channel for a message. * messaging - navigator configured with a pool of channels and performs channel selection based on channel availability and best originator type for a recipient country. The best originator type for a recipient country is determined by the strategy - prioritized list of originator types for each country. At this moment, the default pre-configured strategy (set of country policies) is used see https://docs.bird.com/applications/channels/channels/supported-channels/sms/concepts/choosing-the-right-sender-availability-and-restrictions-by-country |
| `updatedAt` | date |  |
| `workspaceId` | string | The unique identifier of the navigator. |

## Native endpoint

Through the native MessageBird API, this operation is `POST /workspaces/:workspaceId/navigators` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-navigator.md) for the provider-specific parameters and requirements.

