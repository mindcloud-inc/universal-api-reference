# GSA Public Comment: Get Document

Retrieves a specific document from GSA Public Comment.

```
GET https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Public Comment `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | ID of the document to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Use attachments to include attachments in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "agencyId": "string",
          "commentEndDate": "2026-05-07T12:00:00.000Z",
          "commentStartDate": "2026-05-07T12:00:00.000Z",
          "docketId": "string",
          "documentType": "string",
          "fileFormats": [
            {}
          ],
          "frDocNum": "string",
          "objectId": "string",
          "openForComment": true,
          "postedDate": "2026-05-07T12:00:00.000Z",
          "subtype": "string",
          "title": "string",
          "topics": [
            "string"
          ],
          "withinCommentPeriod": true
        },
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "relationships": {
          "attachments": {
            "links": {
              "related": "https://example.com"
            }
          }
        },
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Document resource. |
| `data.attributes.agencyId` | string |  |
| `data.attributes.commentEndDate` | date |  |
| `data.attributes.commentStartDate` | date |  |
| `data.attributes.docketId` | string |  |
| `data.attributes.documentType` | string |  |
| `data.attributes.fileFormats` | array<object> |  |
| `data.attributes.frDocNum` | string |  |
| `data.attributes.objectId` | string |  |
| `data.attributes.openForComment` | boolean |  |
| `data.attributes.postedDate` | date |  |
| `data.attributes.subtype` | string |  |
| `data.attributes.title` | string |  |
| `data.attributes.topics` | array<string> |  |
| `data.attributes.withinCommentPeriod` | boolean |  |
| `data.id` | string | Document ID. |
| `data.links.self` | string |  |
| `data.relationships.attachments.links.related` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native GSA Public Comment API, this operation is `GET /documents/:documentId` (base URL `https://api.regulations.gov/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

