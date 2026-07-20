# Encodian - Utilities: Utilities - Validate Email Address



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-validate-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-validate-email-address?connectionId=$CONNECTION_ID&emailAddress=ava%40example.com&regex=%5E%5B%5E%40%5Cs%5D%2B%40%5B%5E%40%5Cs%5D%2B%5C.%5B%5E%40%5Cs%5D%2B%24" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "ava@example.com",
  "regex": "^[^@\\s]+@[^@\\s]+\\.[^@\\s]+$"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-validate-email-address?${params}`, {
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
| `emailAddress` | string | yes | The email address to verify |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `regex` | string | yes | The regular expression used for validation Default: `^[^@\\s]+@[^@\\s]+\\.[^@\\s]+$`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |
| `result` | boolean | The response value for the request |

## Native endpoint

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/ValidateEmailAddress` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-validate-email-address.md) for the provider-specific parameters and requirements.

