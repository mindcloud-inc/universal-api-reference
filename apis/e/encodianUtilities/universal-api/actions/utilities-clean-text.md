# Encodian - Utilities: Utilities - Clean Text



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-clean-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-clean-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-clean-text?${params}`, {
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
| `text` | string | yes | The text value to process |
| `removeCharacterSet` | string | no | Set the collection of characters to remove from the text value provided |
| `removeControlChars` | boolean | no | Set whether to remove control characters from the text value Default: `false`. |
| `removeInvalidFileNameChars` | boolean | no | Set whether to remove characters that are invalid in file names from the text value Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trimResult` | boolean | no | Set whether white-space should be trimmed from the processed text value Default: `true`. |

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
      "result": "string"
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
| `result` | string | The response value for the request |

## Native endpoint

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/CleanString` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-clean-text.md) for the provider-specific parameters and requirements.

