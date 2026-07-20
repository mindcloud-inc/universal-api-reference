# AltText.Ai: Update Account

Updates your account settings in AltText.Ai.

```
PUT https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AltText.Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/update-account', {
  method: 'PUT',
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
| `name` | string | no | Update the account name. |
| `notificationEmail` | string | no | Set the email address for important account notifications. |
| `webhookUrl` | string | no | Set the default webhook URL for account notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultLang": "string",
      "endingPeriod": true,
      "errors": {},
      "gptPrompt": "string",
      "maxChars": 1,
      "name": "Ava Chen",
      "noQuotes": true,
      "notificationEmail": "ava@example.com",
      "removeSymbols": [
        "string"
      ],
      "subscription": {},
      "usage": 1,
      "usageLimit": 1,
      "webhookUrl": "https://example.com",
      "whitelabel": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultLang` | string |  |
| `endingPeriod` | boolean |  |
| `errors` | object |  |
| `gptPrompt` | string |  |
| `maxChars` | number |  |
| `name` | string |  |
| `noQuotes` | boolean |  |
| `notificationEmail` | string |  |
| `removeSymbols` | array<string> |  |
| `subscription` | object |  |
| `usage` | number |  |
| `usageLimit` | number |  |
| `webhookUrl` | string |  |
| `whitelabel` | boolean |  |

## Native endpoint

Through the native AltText.Ai API, this operation is `PUT /account` (base URL `https://alttext.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

