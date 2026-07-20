# Mindee: Get Split Result

Retrieves a split result from Mindee.

```
GET https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-split-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mindee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-split-result?connectionId=$CONNECTION_ID&inferenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inferenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindee/latest/actions/get-split-result?${params}`, {
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
| `inferenceId` | string | yes | UUID of the inference to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inference": {
        "file": {
          "mime_type": "string",
          "name": "Ava Chen",
          "page_count": 1
        },
        "id": "string",
        "job": {
          "id": "string"
        },
        "model": {
          "id": "string"
        },
        "result": {
          "splits": [
            {
              "document_type": "string",
              "page_range": [
                1
              ]
            }
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inference.file.mime_type` | string |  |
| `inference.file.name` | string |  |
| `inference.file.page_count` | number |  |
| `inference.id` | string |  |
| `inference.job.id` | string |  |
| `inference.model.id` | string |  |
| `inference.result.splits[].document_type` | string |  |
| `inference.result.splits[].page_range[]` | number |  |

## Native endpoint

Through the native Mindee API, this operation is `GET /v2/products/split/results/:inference_id` (base URL `https://api-v2.mindee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-split-result.md) for the provider-specific parameters and requirements.

