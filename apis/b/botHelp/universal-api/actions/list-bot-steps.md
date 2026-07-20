# BotHelp: List Bot Steps

Retrieves step details for a bot in BotHelp.

```
GET https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-bot-steps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BotHelp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-bot-steps?connectionId=$CONNECTION_ID&bot_referral=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bot_referral": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-bot-steps?${params}`, {
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
| `bot_referral` | string | yes | Bot referral identifier from BotHelp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "referral": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `referral` | string | Step referral identifier. |
| `title` | string | Step title. |

## Native endpoint

Through the native BotHelp API, this operation is `GET /v1/bots/:bot_referral/steps` (base URL `https://api.bothelp.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bot-steps.md) for the provider-specific parameters and requirements.

