# Brand.dev: Query Website Data Using AI

Retrieves website answers using AI in Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/query-website-data-using-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/query-website-data-using-ai?connectionId=$CONNECTION_ID&dataToExtract%5B%5D=%5Bobject%20Object%5D&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataToExtract[]": "[object Object]",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/query-website-data-using-ai?${params}`, {
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
| `dataToExtract[]` | array<object> | yes | Array of data points to extract from the website. |
| `domain` | string | yes | Domain name to analyze. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataExtracted": [
        [
          {}
        ]
      ],
      "domain": "string",
      "status": "string",
      "urlsAnalyzed": [
        [
          "https://example.com"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataExtracted[]` | array<object> |  |
| `dataExtracted[].datapointName` | string |  |
| `dataExtracted[].datapointValue` | string |  |
| `domain` | string |  |
| `status` | string |  |
| `urlsAnalyzed[]` | array<string> |  |

## Native endpoint

Through the native Brand.dev API, this operation is `POST /brand/ai/query` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-website-data-using-ai.md) for the provider-specific parameters and requirements.

