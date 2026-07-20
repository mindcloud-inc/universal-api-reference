# Shadify: Verify Kuromasu Puzzle

Retrieves a Kuromasu validation result from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-kuromasu-puzzle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-kuromasu-puzzle?connectionId=$CONNECTION_ID&solution%5B%5D=6%2C4%2Cx%2C4%2C6%2C9%2C7%2C8%2C7%2C9%2C9%2C7%2C8%2C7%2C9%2C5%2Cx%2C4%2Cx%2C5%2C9%2C5%2C8%2C5%2C9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "solution[]": "6,4,x,4,6,9,7,8,7,9,9,7,8,7,9,5,x,4,x,5,9,5,8,5,9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-kuromasu-puzzle?${params}`, {
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
| `solution[]` | array<array> | yes | Required completed Kuromasu grid. Default: `[["6","4","x","4","6"],["9","7","8","7","9"],["9","7","8","7","9"],["5","x","4","x","5"],["9","5","8","5","9"]]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isValid": true,
      "position": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isValid` | boolean | Whether the Kuromasu solution is valid. |
| `position` | object | Invalid row and column position. |

## Native endpoint

Through the native Shadify API, this operation is `POST /kuromasu/verifier` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-kuromasu-puzzle.md) for the provider-specific parameters and requirements.

