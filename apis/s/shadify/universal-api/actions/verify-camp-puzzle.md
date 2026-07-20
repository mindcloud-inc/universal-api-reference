# Shadify: Verify Camp Puzzle

Retrieves a Camp validation result from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-camp-puzzle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-camp-puzzle?connectionId=$CONNECTION_ID&rowTents%5B%5D=1%2C2%2C2%2C1%2C0%2C2%2C1&columnTents%5B%5D=1%2C1%2C0%2C2%2C0%2C2%2C3&solution%5B%5D=0%2C0%2C0%2C1%2C0%2C2%2C1%2C0%2C0%2C0%2C2%2C0%2C1%2C2%2C0%2C2%2C0%2C0%2C0%2C2%2C0%2C0%2C1%2C0%2C0%2C0%2C1%2C2%2C0%2C0%2C0%2C0%2C0%2C0%2C1%2C2%2C0%2C0%2C2%2C0%2C0%2C1%2C1%2C0%2C0%2C1%2C0%2C0%2C2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowTents[]": "1,2,2,1,0,2,1",
  "columnTents[]": "1,1,0,2,0,2,3",
  "solution[]": "0,0,0,1,0,2,1,0,0,0,2,0,1,2,0,2,0,0,0,2,0,0,1,0,0,0,1,2,0,0,0,0,0,0,1,2,0,0,2,0,0,1,1,0,0,1,0,0,2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-camp-puzzle?${params}`, {
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
| `rowTents[]` | array<number> | yes | Required array of tent counts for each row. Default: `[1,2,2,1,0,2,1]`. |
| `columnTents[]` | array<number> | yes | Required array of tent counts for each column. Default: `[1,1,0,2,0,2,3]`. |
| `solution[]` | array<array> | yes | Required completed Camp grid, where 1 values are trees and 2 values are tents. Default: `[[0,0,0,1,0,2,1],[0,0,0,2,0,1,2],[0,2,0,0,0,2,0],[0,1,0,0,0,1,2],[0,0,0,0,0,0,1],[2,0,0,2,0,0,1],[1,0,0,1,0,0,2]]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isValid": true,
      "message": "string",
      "position": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isValid` | boolean | Whether the Camp solution is valid. |
| `message` | string | Validation message. |
| `position` | string | Invalid position. |

## Native endpoint

Through the native Shadify API, this operation is `POST /camp/verifier` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-camp-puzzle.md) for the provider-specific parameters and requirements.

