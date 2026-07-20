# HigherGov: List Opportunity Documents

Retrieves opportunity documents from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-opportunity-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-opportunity-documents?connectionId=$CONNECTION_ID&limit=25&offset=0&relatedKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "relatedKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-opportunity-documents?${params}`, {
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
| `relatedKey` | string | yes | Document key from the Opportunity endpoint document_path field |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "file_name": "Ava Chen",
      "file_size": 1,
      "file_type": "string",
      "posted_date": "string",
      "summary": "string",
      "text_extract": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string |  |
| `file_name` | string |  |
| `file_size` | number |  |
| `file_type` | string |  |
| `posted_date` | string |  |
| `summary` | string |  |
| `text_extract` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/document/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunity-documents.md) for the provider-specific parameters and requirements.

