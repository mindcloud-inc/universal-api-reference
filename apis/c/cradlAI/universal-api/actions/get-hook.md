# Cradl AI: Get Hook

Retrieves a hook from Cradl AI.

```
GET https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-hook?connectionId=$CONNECTION_ID&hookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-hook?${params}`, {
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
| `hookId` | string | yes | Identifier of the hook. |

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

Through the native Cradl AI API, this operation is `GET /hooks/:hookId` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hook.md) for the provider-specific parameters and requirements.

