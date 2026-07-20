# Affinda: Get list of all documents

Retrieves accessible document summaries from Affinda.

```
GET https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Affinda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-documents?${params}`, {
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
| `collection` | string | no | Filter by collection. |
| `compact` | string | no | If "true", the response is compacted to annotations' parsed data. Annotations' meta data are excluded. Default is "false". |
| `count` | string | no | If "false", the documents count is not computed, thus saving time for large collections. Default is "true". |
| `createdDt` | string | no | Filter by created datetime. |
| `customIdentifier` | string | no | Filter for documents with this custom identifier. |
| `exclude` | string | no | Exclude some documents from the result. |
| `failed` | string | no | Filter by failed status. |
| `hasChallenges` | string | no | Filter for documents with challenges. |
| `includeData` | string | no | By default, this endpoint returns only the meta data of the documents. Set this to `true` will return a summary of the data that was parsed. If you want to retrieve the full set of data for a document, use the `GET /documents/{identifier}` endpoint. |
| `inReview` | string | no | Exclude documents that are currently being reviewed. |
| `limit` | string | no | The numbers of results to return. |
| `offset` | string | no | The number of documents to skip before starting to collect the result set. |
| `ordering` | string | no | Sort the result set. A "-" at the beginning denotes DESC sort, e.g. -created_dt. Sort by multiple fields is supported. Supported values include: 'file_name', 'extractor', 'created_dt', 'validated_dt', 'archived_dt' and 'parsed__<dataPointSlug>'. |
| `ready` | string | no | Filter by ready status. |
| `search` | string | no | Partial, case-insensitive match with file name or tag name. |
| `snakeCase` | string | no | Whether to return the response in snake_case instead of camelCase. Default is false. |
| `state` | string | no | Filter by the document's state. |
| `tags` | string | no | Filter by tag's IDs. |
| `validatable` | string | no | Filter for validatable documents. |
| `workspace` | string | no | Filter by workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": {},
      "extractor": "string",
      "meta": {},
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | object |  |
| `extractor` | string |  |
| `meta` | object |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Affinda API, this operation is `GET /v3/documents` (base URL `https://api.us1.affinda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

