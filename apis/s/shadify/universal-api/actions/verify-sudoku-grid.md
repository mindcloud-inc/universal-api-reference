# Shadify: Verify Sudoku Grid

Retrieves a Sudoku validation result from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-sudoku-grid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-sudoku-grid?connectionId=$CONNECTION_ID&task%5B%5D=1%2C2%2C3%2C4%2C5%2C6%2C7%2C8%2C9%2C4%2C5%2C6%2C7%2C8%2C9%2C1%2C2%2C3%2C7%2C8%2C9%2C1%2C2%2C3%2C4%2C5%2C6%2C2%2C3%2C4%2C5%2C6%2C7%2C8%2C9%2C1%2C5%2C6%2C7%2C8%2C9%2C1%2C2%2C3%2C4%2C8%2C9%2C1%2C2%2C3%2C4%2C5%2C6%2C7%2C3%2C4%2C5%2C6%2C7%2C8%2C9%2C1%2C2%2C6%2C7%2C8%2C9%2C1%2C2%2C3%2C4%2C5%2C9%2C1%2C2%2C3%2C4%2C5%2C6%2C7%2C8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task[]": "1,2,3,4,5,6,7,8,9,4,5,6,7,8,9,1,2,3,7,8,9,1,2,3,4,5,6,2,3,4,5,6,7,8,9,1,5,6,7,8,9,1,2,3,4,8,9,1,2,3,4,5,6,7,3,4,5,6,7,8,9,1,2,6,7,8,9,1,2,3,4,5,9,1,2,3,4,5,6,7,8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-sudoku-grid?${params}`, {
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
| `task[]` | array<array> | yes | Required solved Sudoku grid as a 9x9 array of numbers. Default: `[[1,2,3,4,5,6,7,8,9],[4,5,6,7,8,9,1,2,3],[7,8,9,1,2,3,4,5,6],[2,3,4,5,6,7,8,9,1],[5,6,7,8,9,1,2,3,4],[8,9,1,2,3,4,5,6,7],[3,4,5,6,7,8,9,1,2],[6,7,8,9,1,2,3,4,5],[9,1,2,3,4,5,6,7,8]]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isValid": true,
      "position": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isValid` | boolean | Whether the Sudoku task is valid. |
| `position` | string | Error position, or an empty string when valid. |

## Native endpoint

Through the native Shadify API, this operation is `POST /sudoku/verifier` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-sudoku-grid.md) for the provider-specific parameters and requirements.

