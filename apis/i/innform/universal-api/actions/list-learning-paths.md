# Innform: List Learning Paths

Retrieves learning paths from Innform.

```
GET https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-learning-paths
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-learning-paths?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-learning-paths?${params}`, {
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
      "blended": true,
      "courses": [
        {}
      ],
      "description": "string",
      "id": "string",
      "points": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blended` | boolean | Whether the learning path is blended. |
| `courses` | array<object> | Courses included in the learning path. |
| `description` | string | Learning path description. |
| `id` | string | Learning path ID. |
| `points` | number | Learning path points. |
| `title` | string | Learning path title. |

## Native endpoint

Through the native Innform API, this operation is `GET /learning_paths` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-learning-paths.md) for the provider-specific parameters and requirements.

