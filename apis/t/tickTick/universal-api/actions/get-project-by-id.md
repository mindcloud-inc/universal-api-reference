# TickTick: Get Project By ID

Retrieves a project from TickTick by ID.

```
GET https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-project-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TickTick `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-project-by-id?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tickTick/latest/actions/get-project-by-id?${params}`, {
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
| `projectId` | list<string> | yes | Project identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closed": true,
      "color": "string",
      "groupId": "string",
      "id": "string",
      "kind": "string",
      "name": "Ava Chen",
      "permission": "string",
      "sortOrder": 1,
      "viewMode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | boolean |  |
| `color` | string |  |
| `groupId` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `name` | string |  |
| `permission` | string |  |
| `sortOrder` | number |  |
| `viewMode` | string |  |

## Native endpoint

Through the native TickTick API, this operation is `GET /open/v1/project/:projectId` (base URL `https://api.ticktick.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-by-id.md) for the provider-specific parameters and requirements.

