# Automatic Data Extraction: Process Custom PUT Request

Processes a custom PUT request in Automatic Data Extraction.

```
GET https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/process-custom-put-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Automatic Data Extraction `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/process-custom-put-request?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/automaticDataExtraction/latest/actions/process-custom-put-request?${params}`, {
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
| `url` | string | yes | Absolute URL to extract data from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "httpResponseBody": "string",
      "httpResponseHeaders": [
        {}
      ],
      "statusCode": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `httpResponseBody` | string |  |
| `httpResponseHeaders` | array<object> |  |
| `statusCode` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Automatic Data Extraction API, this operation is `POST /extract` (base URL `https://api.zyte.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-custom-put-request.md) for the provider-specific parameters and requirements.

