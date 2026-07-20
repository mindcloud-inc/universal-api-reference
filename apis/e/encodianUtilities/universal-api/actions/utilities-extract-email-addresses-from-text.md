# Encodian - Utilities: Utilities - Extract Email Addresses from Text



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-email-addresses-from-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-email-addresses-from-text?connectionId=$CONNECTION_ID&text=string&regex=%5CS%2B%3F%40%5CS%2B%3F%5C.%5CS%2B" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string",
  "regex": "\\S+?@\\S+?\\.\\S+"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-email-addresses-from-text?${params}`, {
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
| `text` | string | yes | The text from which email addresses are to be extracted |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `regex` | string | yes | The default regular expression used for extraction Default: `\\S+?@\\S+?\\.\\S+`. |

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
      "result": [
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
| `errors` | array<string> |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |
| `result` | array<string> | The response value for the request |

## Native endpoint

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/ExtractEmailAddressesFromText` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-extract-email-addresses-from-text.md) for the provider-specific parameters and requirements.

