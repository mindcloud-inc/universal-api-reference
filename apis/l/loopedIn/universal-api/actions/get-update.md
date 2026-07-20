# LoopedIn: Get Update

Retrieves an update from LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-update?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/get-update?${params}`, {
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
| `id` | string | yes | The LoopedIn update ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "category": {},
      "created": "string",
      "dislikes": 1,
      "id": "string",
      "likes": 1,
      "neutrals": 1,
      "pinned": true,
      "public": true,
      "published": "string",
      "status": "string",
      "title": "string",
      "updated": "string",
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
| `category` | object |  |
| `created` | string |  |
| `dislikes` | number |  |
| `id` | string |  |
| `likes` | number |  |
| `neutrals` | number |  |
| `pinned` | boolean |  |
| `public` | boolean |  |
| `published` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updated` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /updates/:id` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-update.md) for the provider-specific parameters and requirements.

