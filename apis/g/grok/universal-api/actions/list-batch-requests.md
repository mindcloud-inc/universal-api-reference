# Grok: List Batch Requests

Retrieves a list of requests in a Grok batch.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-batch-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-batch-requests?connectionId=$CONNECTION_ID&batchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "batchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/list-batch-requests?${params}`, {
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
| `batchId` | string | yes | Batch identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchRequestMetadata": [
        {
          "batchRequestId": "string",
          "state": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchRequestMetadata` | array<object> | Metadata for requests currently attached to the batch. |
| `batchRequestMetadata[].batchRequestId` | string | Batch request identifier. |
| `batchRequestMetadata[].state` | string | Current lifecycle state for the batch request. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/batches/:batch_id/requests` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-batch-requests.md) for the provider-specific parameters and requirements.

