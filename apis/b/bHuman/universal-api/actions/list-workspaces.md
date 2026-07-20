# BHuman: List Workspaces

Retrieves available account workspaces from BHuman.

```
GET https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-workspaces?${params}`, {
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
| `id` | string | no | Optional workspace ID filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "result": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": 1,
          "name": "Ava Chen",
          "role": "string",
          "token": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "userId": "string",
          "workspaceId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `result[].createdAt` | date |  |
| `result[].description` | string |  |
| `result[].id` | number |  |
| `result[].name` | string |  |
| `result[].role` | string |  |
| `result[].token` | string |  |
| `result[].updatedAt` | date |  |
| `result[].userId` | string |  |
| `result[].workspaceId` | string |  |

## Native endpoint

Through the native BHuman API, this operation is `GET https://user.bhuman.ai/api/workspace` (base URL `https://studio.bhuman.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

