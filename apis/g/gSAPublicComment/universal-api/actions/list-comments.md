# GSA Public Comment: List Comments

Retrieves a list of comments from GSA Public Comment.

```
GET https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Public Comment `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/list-comments?${params}`, {
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
| `agencyId` | string | no | Filter comments by agency acronym, such as EPA. |
| `searchTerm` | string | no | Filter comments by keyword or identifier. |
| `commentOnId` | string | no | Filter comments by the objectId of the document being commented on. |
| `postedDate` | date | no | Filter comments by posted date in yyyy-MM-dd format. |
| `lastModifiedDate` | date | no | Filter comments by last modified date in yyyy-MM-dd HH:mm:ss format. |

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
            "documentType": "string",
            "objectId": "string",
            "postedDate": "2026-05-07T12:00:00.000Z",
            "title": "string",
            "withdrawn": true
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
| `data` | array<object> | Comment resources. |
| `data[].attributes.agencyId` | string |  |
| `data[].attributes.documentType` | string |  |
| `data[].attributes.objectId` | string |  |
| `data[].attributes.postedDate` | date |  |
| `data[].attributes.title` | string |  |
| `data[].attributes.withdrawn` | boolean |  |
| `data[].id` | string | Comment ID. |
| `data[].links.self` | string |  |
| `data[].type` | string |  |
| `meta.hasNextPage` | boolean |  |
| `meta.hasPreviousPage` | boolean |  |
| `meta.pageNumber` | number |  |
| `meta.pageSize` | number |  |
| `meta.totalElements` | number |  |
| `meta.totalPages` | number |  |

## Native endpoint

Through the native GSA Public Comment API, this operation is `GET /comments` (base URL `https://api.regulations.gov/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

