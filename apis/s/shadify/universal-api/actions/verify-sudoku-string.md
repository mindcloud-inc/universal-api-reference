# Shadify: Verify Sudoku String

Retrieves a Sudoku validation result from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-sudoku-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-sudoku-string?connectionId=$CONNECTION_ID&task=123456789-456789123-789123456-234567891-567891234-891234567-345678912-678912345-912345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task": "123456789-456789123-789123456-234567891-567891234-891234567-345678912-678912345-912345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/verify-sudoku-string?${params}`, {
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
| `task` | string | yes | Required Sudoku rows joined by dashes, such as 123-123-123. Default: `123456789-456789123-789123456-234567891-567891234-891234567-345678912-678912345-912345678`. |

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

Through the native Shadify API, this operation is `GET /sudoku/verifier` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-sudoku-string.md) for the provider-specific parameters and requirements.

