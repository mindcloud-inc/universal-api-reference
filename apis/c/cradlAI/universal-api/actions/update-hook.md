# Cradl AI: Update Hook

Updates an existing hook in Cradl AI.

```
PUT https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-hook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hookId` | string | yes | Identifier of the hook to update. |
| `name` | string | no | Updated hook name. |
| `description` | string | no | Updated hook description. |
| `trigger` | list | no | Updated trigger type for the hook. One of: `ActionRun has Completed`, `Document is Created`, `Email is Received`, `Prediction is Created`, `ValidationTask has Completed`, `ValidationTask is Created`. |
| `enabled` | boolean | no | Whether the hook is enabled. |
| `functionId` | string | no | Updated function identifier used by the hook. |
| `trueActionId` | string | no | Updated action to run when the hook evaluates true. |
| `falseActionId` | string | no | Updated action to run when the hook evaluates false. |
| `config` | object | no | Updated hook configuration object. |
| `metadata` | object | no | Updated metadata attached to the hook. |

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

Through the native Cradl AI API, this operation is `PATCH /hooks/:hookId` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-hook.md) for the provider-specific parameters and requirements.

