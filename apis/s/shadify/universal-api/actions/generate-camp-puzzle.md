# Shadify: Generate Camp Puzzle

Retrieves a random Camp puzzle from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-camp-puzzle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-camp-puzzle?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-camp-puzzle?${params}`, {
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
| `width` | number | no | Optional puzzle width from 5 to 15. Default is 7. Default: `7`. |
| `height` | number | no | Optional puzzle height from 5 to 15. Default is 7. Default: `7`. |
| `solution` | boolean | no | Optional true or false value that includes the solution. Default is true. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columnTents": [
        1
      ],
      "height": 1,
      "rowTents": [
        1
      ],
      "solution": [
        [
          "string"
        ]
      ],
      "task": [
        [
          "string"
        ]
      ],
      "trees": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnTents` | array<number> | Tent counts per column. |
| `height` | number | Puzzle height. |
| `rowTents` | array<number> | Tent counts per row. |
| `solution` | array<array> | Solved puzzle grid. |
| `task` | array<array> | Puzzle task grid. |
| `trees` | number | Tree count. |
| `width` | number | Puzzle width. |

## Native endpoint

Through the native Shadify API, this operation is `GET /camp/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-camp-puzzle.md) for the provider-specific parameters and requirements.

