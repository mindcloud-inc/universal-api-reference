# Voiceflow: Search Documents

Finds knowledge base documents in Voiceflow.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/search-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/search-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/search-documents?${params}`, {
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
| `page` | number | no | Page number to retrieve. Default: `1`. Example: `1`. |
| `limit` | number | no | Number of documents to return per page. Default: `10`. Example: `10`. |
| `documentType` | string | no | Filter documents by type. Example: `table`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> | Matching document summaries. |
| `total` | number | Total matching documents. |

## Native endpoint

Through the native Voiceflow API, this operation is `GET https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-documents.md) for the provider-specific parameters and requirements.

