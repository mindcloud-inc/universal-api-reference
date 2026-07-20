# Shadify: Verify Takuzu Grid

Retrieves a Takuzu validation result from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-takuzu-grid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-takuzu-grid?connectionId=$CONNECTION_ID&task%5B%5D=1%2C0%2C1%2C0%2C1%2C1%2C0%2C0%2C0%2C0%2C1%2C1%2C0%2C1%2C0%2C1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task[]": "1,0,1,0,1,1,0,0,0,0,1,1,0,1,0,1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-takuzu-grid?${params}`, {
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
| `task[]` | array<array> | yes | Required Takuzu grid as a square array of 0 and 1 strings. Default: `[["1","0","1","0"],["1","1","0","0"],["0","0","1","1"],["0","1","0","1"]]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isValid": true,
      "message": "string",
      "position": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isValid` | boolean | Whether the Takuzu task is valid. |
| `message` | string | Validation message. |
| `position` | array<string> | Affected rows or columns. |

## Native endpoint

Through the native Shadify API, this operation is `POST /takuzu/verifier` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-takuzu-grid.md) for the provider-specific parameters and requirements.

