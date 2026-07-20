# Shadify: Generate Memory Grid

Retrieves a random memory grid from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-memory-grid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-memory-grid?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-memory-grid?${params}`, {
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
| `width` | number | no | Optional grid width. Default is 6. Default: `6`. |
| `height` | number | no | Optional grid height. Default is 4. Default: `4`. |
| `pairSize` | number | no | Optional matching group size. Available values are 2, 3, and 4. Default is 3. Default: `3`. |
| `showPositions` | boolean | no | Optional true or false value that includes positions for each pair. Default is true. Default: `true`. |

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
      "height": 1,
      "pairPositions": [
        {}
      ],
      "pairSize": 1,
      "totalPairs": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `grid` | array<array> | Memory grid. |
| `height` | number | Grid height. |
| `pairPositions` | array<object> | Positions for each value. |
| `pairSize` | number | Pair size. |
| `totalPairs` | number | Total number of pairs. |
| `width` | number | Grid width. |

## Native endpoint

Through the native Shadify API, this operation is `GET /memory/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-memory-grid.md) for the provider-specific parameters and requirements.

