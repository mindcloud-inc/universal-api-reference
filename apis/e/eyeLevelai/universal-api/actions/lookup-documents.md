# EyeLevel.ai: Lookup Documents

Retrieves documents in EyeLevel.ai by process, bucket, or group.

```
GET https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/lookup-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EyeLevel.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/lookup-documents?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/lookup-documents?${params}`, {
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
| `id` | string | yes | A processId, bucketId, or groupId whose associated documents should be listed. |
| `n` | number | no | The maximum number of returned documents. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "documents": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of documents returned in this page. |
| `documents` | array<object> | Documents matching the lookup. |
| `total` | number | Total matched documents. |

## Native endpoint

Through the native EyeLevel.ai API, this operation is `GET /ingest/documents/:id` (base URL `https://api.groundx.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-documents.md) for the provider-specific parameters and requirements.

