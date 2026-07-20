# Chroma Cloud: Get indexing status

Retrieves collection indexing status from Chroma Cloud.

```
GET https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-indexing-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-indexing-status?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-indexing-status?${params}`, {
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
| `collectionId` | string | yes | Collection UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "num_indexed_ops": 1,
      "num_unindexed_ops": 1,
      "op_indexing_progress": 1,
      "total_ops": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `num_indexed_ops` | number |  |
| `num_unindexed_ops` | number |  |
| `op_indexing_progress` | number |  |
| `total_ops` | number |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `GET /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/indexing_status` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indexing-status.md) for the provider-specific parameters and requirements.

