# BotHunter: Remove User From Bot

Deletes a BotHunter bot enrollment for a user in a specified channel.

```
DELETE https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/remove-user-from-bot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/remove-user-from-bot?connectionId=$CONNECTION_ID&botId=607d97c6a01c6a25972ed95e&uid=102036383&channel=VK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "607d97c6a01c6a25972ed95e",
  "uid": "102036383",
  "channel": "VK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/remove-user-from-bot?${params}`, {
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
| `botId` | string | yes | ID of the BotHunter bot to remove the user from. Example: `607d97c6a01c6a25972ed95e`. |
| `uid` | string | yes | User ID in the social network or messenger channel. Example: `102036383`. |
| `channel` | list<string> | yes | Channel identifier. Documented values: VK, TG, MAX, OK. One of: `MAX`, `OK`, `TG`, `VK`. Example: `VK`. |

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
| `success` | boolean | Whether BotHunter accepted the remove-user request. |
| `uid` | string | Social or messenger user ID used in the request. |

## Native endpoint

Through the native BotHunter API, this operation is `POST /bots/removeUser` (base URL `https://smm.targethunter.ru/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-bot.md) for the provider-specific parameters and requirements.

