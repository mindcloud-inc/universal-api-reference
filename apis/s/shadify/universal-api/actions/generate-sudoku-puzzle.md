# Shadify: Generate Sudoku Puzzle

Retrieves a random Sudoku puzzle from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-sudoku-puzzle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-sudoku-puzzle?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-sudoku-puzzle?${params}`, {
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
| `fill` | number | no | Optional fill level from 0 to 50 percent. Default is 30. Default: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "grid": [
        [
          "string"
        ]
      ],
      "task": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `grid` | array<array> | Fully solved Sudoku grid. |
| `task` | array<array> | Puzzle grid with zeroes to fill. |

## Native endpoint

Through the native Shadify API, this operation is `GET /sudoku/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-sudoku-puzzle.md) for the provider-specific parameters and requirements.

