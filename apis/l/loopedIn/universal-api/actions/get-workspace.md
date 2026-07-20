# LoopedIn: Get Workspace

Retrieves a workspace from LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-workspace?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-workspace?${params}`, {
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
| `id` | string | yes | The LoopedIn workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "created": "string",
      "guid": "string",
      "id": "string",
      "roadmap": "string",
      "slug": "string",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `created` | string |  |
| `guid` | string |  |
| `id` | string |  |
| `roadmap` | string |  |
| `slug` | string |  |
| `title` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /workspaces/:id` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

