# GSA Public Comment: List Documents

Retrieves a list of documents from GSA Public Comment.

```
GET https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Public Comment `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-documents?${params}`, {
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
| `agencyId` | string | no | Filter documents by agency acronym, such as EPA. |
| `searchTerm` | string | no | Filter documents by keyword or identifier. |
| `docketId` | string | no | Filter documents by docket ID. |
| `documentType` | string | no | Filter documents by document type. |
| `frDocNum` | string | no | Filter documents by Federal Register document number. |
| `postedDate` | date | no | Filter documents by posted date in yyyy-MM-dd format. |
| `commentEndDate` | date | no | Filter documents by comment end date in yyyy-MM-dd format. |
| `lastModifiedDate` | date | no | Filter documents by last modified date in yyyy-MM-dd HH:mm:ss format. |
| `subtype` | string | no | Filter documents by subtype. |
| `withinCommentPeriod` | boolean | no | Set to true to return documents open for comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "agencyId": "string",
            "docketId": "string",
            "documentType": "string",
            "objectId": "string",
            "openForComment": true,
            "postedDate": "2026-05-07T12:00:00.000Z",
            "title": "string",
            "withinCommentPeriod": true
          },
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "type": "string"
        }
      ],
      "meta": {
        "hasNextPage": true,
        "hasPreviousPage": true,
        "pageNumber": 1,
        "pageSize": 1,
        "totalElements": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Document resources. |
| `data[].attributes.agencyId` | string |  |
| `data[].attributes.docketId` | string |  |
| `data[].attributes.documentType` | string |  |
| `data[].attributes.objectId` | string |  |
| `data[].attributes.openForComment` | boolean |  |
| `data[].attributes.postedDate` | date |  |
| `data[].attributes.title` | string |  |
| `data[].attributes.withinCommentPeriod` | boolean |  |
| `data[].id` | string | Document ID. |
| `data[].links.self` | string |  |
| `data[].type` | string | JSON:API resource type. |
| `meta.hasNextPage` | boolean |  |
| `meta.hasPreviousPage` | boolean |  |
| `meta.pageNumber` | number |  |
| `meta.pageSize` | number |  |
| `meta.totalElements` | number |  |
| `meta.totalPages` | number |  |

## Native endpoint

Through the native GSA Public Comment API, this operation is `GET /documents` (base URL `https://api.regulations.gov/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

