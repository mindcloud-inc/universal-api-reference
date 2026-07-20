# BotHunter: Add User To Bot

Creates a BotHunter bot enrollment for a user in a specified channel.

```
POST https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/add-user-to-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/add-user-to-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "607d97c6a01c6a25972ed95e",
  "uid": "102036383",
  "channel": "VK"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/add-user-to-bot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "607d97c6a01c6a25972ed95e",
    "uid": "102036383",
    "channel": "VK"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | string | yes | ID of the BotHunter bot to add the user to. Example: `607d97c6a01c6a25972ed95e`. |
| `uid` | string | yes | User ID in the social network or messenger channel. Example: `102036383`. |
| `channel` | list<string> | yes | Channel identifier. Documented values: VK, TG, MAX, OK. One of: `MAX`, `OK`, `TG`, `VK`. Example: `VK`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stepId` | string | no | Optional BotHunter step ID to add the user to. Example: `61af67fb5bc8635f3f53b18b`. |
| `force` | list<string> | no | Use 1 to add the user even if they are already in the bot; use 0 otherwise. One of: `0`, `1`. Example: `0`. |
| `payload` | object | no | Optional additional parameters to pass into the bot. BotHunter accepts a string or structured payload. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": "string",
      "channel": "string",
      "message": "string",
      "success": true,
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | string | Bot ID used in the request. |
| `channel` | string | Channel code used in the request. |
| `message` | string | Provider message, when returned. |
| `success` | boolean | Whether BotHunter accepted the add-user request. |
| `uid` | string | Social or messenger user ID used in the request. |

## Native endpoint

Through the native BotHunter API, this operation is `POST /bots/addUser` (base URL `https://smm.targethunter.ru/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-bot.md) for the provider-specific parameters and requirements.

