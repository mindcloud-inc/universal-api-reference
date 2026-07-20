# Cradl AI: Create Hook

Creates a new hook in Cradl AI.

```
POST https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-hook', {
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
| `name` | string | no | Hook name. |
| `description` | string | no | Hook description. |
| `trigger` | list | no | Trigger type for the hook. One of: `ActionRun has Completed`, `Document is Created`, `Email is Received`, `Prediction is Created`, `ValidationTask has Completed`, `ValidationTask is Created`. |
| `enabled` | boolean | no | Whether the hook is enabled. |
| `functionId` | string | no | Function identifier used by the hook. |
| `trueActionId` | string | no | Action to run when the hook evaluates true. |
| `falseActionId` | string | no | Action to run when the hook evaluates false. |
| `config` | object | no | Hook configuration object. |
| `metadata` | object | no | Metadata attached to the hook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "enabled": true,
      "falseActionId": "string",
      "functionId": "string",
      "hookId": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "trigger": "string",
      "trueActionId": "string",
      "updatedBy": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `createdBy` | string |  |
| `createdTime` | date |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `falseActionId` | string |  |
| `functionId` | string |  |
| `hookId` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `trigger` | string |  |
| `trueActionId` | string |  |
| `updatedBy` | string |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Cradl AI API, this operation is `POST /hooks` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-hook.md) for the provider-specific parameters and requirements.

