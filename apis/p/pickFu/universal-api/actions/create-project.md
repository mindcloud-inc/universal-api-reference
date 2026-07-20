# PickFu: Create Project



```
POST https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/create-project', {
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
| `name` | string | no | Project name. |
| `description` | string | no | Project description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "bookmarked": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "goal": "string",
      "id": "string",
      "name": "Ava Chen",
      "surveys": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `bookmarked` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `goal` | string |  |
| `id` | string |  |
| `name` | string |  |
| `surveys` | array<object> |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native PickFu API, this operation is `POST /projects` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

