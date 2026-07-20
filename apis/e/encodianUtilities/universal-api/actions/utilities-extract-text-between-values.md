# Encodian - Utilities: Utilities - Extract Text between Values



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-text-between-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-text-between-values?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-extract-text-between-values?${params}`, {
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
| `text` | string | yes | The text from which a value is to be extracted |
| `startValue` | string | no | The text value to start the extraction from |
| `endValue` | string | no | The text value to end the extraction from |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreCase` | boolean | no | Set whether the text case should be ignored when executing the extraction Default: `true`. |
| `includeValues` | string | no | Set whether any or both of the 'Start Value' and 'End Value' should be included within the result One of: `0`, `1`, `2`, `3`. Default: `None`. |
| `trimResult` | boolean | no | Set whether white-space should be trimmed from the extracted string Default: `true`. |

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

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/ExtractTextBetweenValues` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-extract-text-between-values.md) for the provider-specific parameters and requirements.

