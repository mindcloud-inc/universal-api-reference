# Shadify: Generate Minesweeper Field

Retrieves a random Minesweeper field from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-minesweeper-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-minesweeper-field?connectionId=$CONNECTION_ID&start=1-1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "1-1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-minesweeper-field?${params}`, {
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
| `start` | string | yes | Required starting position as x-y. Mines are excluded around this position. Default: `1-1`. |
| `width` | number | no | Optional field width. Width times height must not exceed 1000. Default is 9. Default: `9`. |
| `height` | number | no | Optional field height. Width times height must not exceed 1000. Default is 9. Default: `9`. |
| `mines` | number | no | Optional mine count, up to 25 percent of cells. Default is 12. Default: `12`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board": [
        [
          "string"
        ]
      ],
      "height": 1,
      "mines": 1,
      "start": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `board` | array<array> | Generated minesweeper board. |
| `height` | number | Field height. |
| `mines` | number | Mine count. |
| `start` | string | Safe starting position. |
| `width` | number | Field width. |

## Native endpoint

Through the native Shadify API, this operation is `GET /minesweeper/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-minesweeper-field.md) for the provider-specific parameters and requirements.

