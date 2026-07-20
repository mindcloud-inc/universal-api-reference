# Encodian - Utilities: Utilities - Text Contains Value



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-text-contains-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-text-contains-value?connectionId=$CONNECTION_ID&text=string&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-text-contains-value?${params}`, {
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
| `text` | string | yes | The text to validate |
| `value` | string | yes | The value to check is contained within the 'Text' value |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreCase` | boolean | no | Set whether text case should be ignored when validating the 'Text' value Default: `false`. |
| `comparisonConfiguration` | string | no | Specifies the rules to be used when processing the text values provided One of: `0`, `1`, `2`. Default: `CurrentCulture`. |
| `cultureName` | string | no | Change the thread culture used to process the request |

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

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/TextContainsValue` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-text-contains-value.md) for the provider-specific parameters and requirements.

