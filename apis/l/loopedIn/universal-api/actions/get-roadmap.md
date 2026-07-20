# LoopedIn: Get Roadmap

Retrieves a roadmap from LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-roadmap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-roadmap?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-roadmap?${params}`, {
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
| `id` | string | yes | The LoopedIn roadmap ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "columns": [
        {}
      ],
      "id": "string",
      "title": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `columns` | array<object> |  |
| `id` | string |  |
| `title` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /roadmaps/:id` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-roadmap.md) for the provider-specific parameters and requirements.

