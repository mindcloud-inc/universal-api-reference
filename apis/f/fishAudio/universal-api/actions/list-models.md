# Fish Audio: List Models

Retrieves voice models from Fish Audio.

```
GET https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fish Audio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/list-models?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fishAudio/latest/actions/list-models?${params}`, {
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
| `title` | string | no | Filter models by title. |
| `tag[]` | array<string> | no | Filter models by tag. |
| `self` | boolean | no | When true, return only models created by the authenticated user. Default: `false`. |
| `authorId` | string | no | Filter models by author ID when self is false. |
| `language[]` | array<string> | no | Filter models by language. |
| `titleLanguage[]` | array<string> | no | Filter models by title language. |
| `sortBy` | list | no | Sort models by score, task count, or creation time. One of: `0`, `1`, `2`. Default: `score`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Fish Audio API, this operation is `GET /model` (base URL `https://api.fish.audio`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

