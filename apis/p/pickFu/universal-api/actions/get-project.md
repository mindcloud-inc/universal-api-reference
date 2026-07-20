# PickFu: Get Project



```
GET https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | Project GUID. |

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
      "url": "https://example.com",
      "user": "string"
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
| `user` | string |  |

## Native endpoint

Through the native PickFu API, this operation is `GET /projects/[:id]` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

