# Pinecone: Get Index Stats

Retrieves statistics for a Pinecone index.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/get-index-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/get-index-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/get-index-stats?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | object | no | A metadata filter to limit returned stats on supported indexes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dimension": 1,
      "indexFullness": 1,
      "memoryFullness": 1,
      "metric": "string",
      "storageFullness": 1,
      "totalVectorCount": 1,
      "vectorType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimension` | number |  |
| `indexFullness` | number |  |
| `memoryFullness` | number |  |
| `metric` | string |  |
| `storageFullness` | number |  |
| `totalVectorCount` | number |  |
| `vectorType` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `POST {{credentials.indexHost}}/describe_index_stats` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-index-stats.md) for the provider-specific parameters and requirements.

