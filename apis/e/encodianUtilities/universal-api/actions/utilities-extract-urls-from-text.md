# Encodian - Utilities: Utilities - Extract URLs from Text



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-urls-from-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-urls-from-text?connectionId=$CONNECTION_ID&text=string&regex=%5Cb(%3F%3Ahttps%3F%3A%2F%2F%7Cwww%5C.)%5B%5E%5Cs%3C%3E%22%5D%2B%5B%5E.%2C%3B%3A%5Cs%3C%3E%22)%5C%5D%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string",
  "regex": "\\b(?:https?://|www\\.)[^\\s<>\"]+[^.,;:\\s<>\")\\]]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-urls-from-text?${params}`, {
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
| `text` | string | yes | The text from which URL's are to be extracted |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `regex` | string | yes | The default regular expression used for extraction Default: `\\b(?:https?://\|www\\.)[^\\s<>\"]+[^.,;:\\s<>\")\\]]`. |

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

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/ExtractUrlsFromText` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-extract-urls-from-text.md) for the provider-specific parameters and requirements.

