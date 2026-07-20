# Cradl AI: List Hooks

Retrieves all hooks from Cradl AI.

```
GET https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-hooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-hooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-hooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Cradl AI API, this operation is `GET /hooks` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hooks.md) for the provider-specific parameters and requirements.

