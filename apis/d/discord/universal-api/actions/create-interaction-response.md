# Discord: Create Interaction Response

Creates an interaction response in Discord.

```
POST https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-interaction-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-interaction-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "interactionId": "123456789012345678",
  "interactionToken": "interaction-token",
  "type": "4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-interaction-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "interactionId": "123456789012345678",
    "interactionToken": "interaction-token",
    "type": "4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `interactionId` | string | yes | Interaction ID Example: `123456789012345678`. |
| `interactionToken` | string | yes | Interaction token Example: `interaction-token`. |
| `type` | number | yes | Interaction callback type Example: `4`. |
| `data` | object | no | Interaction callback data object |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `withResponse` | boolean | no | Return interaction callback response body Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "interaction": {},
      "resource": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interaction` | object |  |
| `resource` | object |  |

## Native endpoint

Through the native Discord API, this operation is `POST /interactions/:interactionId/:interactionToken/callback` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-interaction-response.md) for the provider-specific parameters and requirements.

