# Encodian - Utilities: Utilities - Split Text



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-split-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-split-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-split-text?${params}`, {
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
| `splitValue` | string | no | Set the value to split the text provided on |
| `splitOn` | string | no | Set whether the text should be split on all instances, the first instance or the last instance of the 'Split Value' One of: `0`, `1`, `2`. Default: `All`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trimResult` | boolean | no | Set whether white-space should be trimmed from the values split from the text provided Default: `true`. |
| `removeEmptyValues` | boolean | no | Set whether empty or null values should be removed from the array of values returned Default: `true`. |
| `preserveSplitValue` | boolean | no | Set whether to preserve the 'Split Value' in each split item returned Default: `false`. |

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

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/SplitText` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-split-text.md) for the provider-specific parameters and requirements.

