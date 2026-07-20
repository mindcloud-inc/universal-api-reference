# eGain: Create Account

Creates a new account in eGain.

```
POST https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "address": "string",
  "channel.id": "string",
  "chatConfigurations.entryPoint.id": "string",
  "chatConfigurations.orchestration.id": "string",
  "chatConfigurations.timeout": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": true,
    "address": "string",
    "channel.id": "string",
    "chatConfigurations.entryPoint.id": "string",
    "chatConfigurations.orchestration.id": "string",
    "chatConfigurations.timeout": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | yes | Whether the account is active. |
| `address` | string | yes | Account address or identifier. |
| `channel.id` | string | yes | Channel ID. |
| `chatConfigurations.defaultLanguage` | string | no | Default language. |
| `chatConfigurations.entryPoint.id` | string | yes | Entry point ID. |
| `chatConfigurations.orchestration.id` | string | yes | Orchestration ID. |
| `chatConfigurations.timeout` | number | yes | Conversation timeout in minutes. |
| `description` | string | no | Account description. |
| `name` | string | yes | Account name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eGain API returns.

## Native endpoint

Through the native eGain API, this operation is `POST /accounts` (base URL `https://api.ai.egain.cloud/conversation/conversationmgr/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account.md) for the provider-specific parameters and requirements.

