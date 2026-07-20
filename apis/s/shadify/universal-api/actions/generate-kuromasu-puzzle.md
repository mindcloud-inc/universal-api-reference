# Shadify: Generate Kuromasu Puzzle

Retrieves a random Kuromasu puzzle from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-kuromasu-puzzle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-kuromasu-puzzle?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-kuromasu-puzzle?${params}`, {
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
| `width` | number | no | Optional grid width from 4 to 15. Default is 5. Default: `5`. |
| `height` | number | no | Optional grid height from 4 to 15. Default is 5. Default: `5`. |
| `fill` | number | no | Optional ready-cell fill level from 10 to 50 percent. Default is 30. Default: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "height": 1,
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
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `height` | number | Grid height. |
| `solution` | array<array> | Solved grid. |
| `task` | array<array> | Kuromasu task grid. |
| `width` | number | Grid width. |

## Native endpoint

Through the native Shadify API, this operation is `GET /kuromasu/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-kuromasu-puzzle.md) for the provider-specific parameters and requirements.

