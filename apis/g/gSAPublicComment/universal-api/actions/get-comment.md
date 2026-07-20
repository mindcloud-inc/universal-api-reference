# GSA Public Comment: Get Comment

Retrieves a specific comment from GSA Public Comment.

```
GET https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Public Comment `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-comment?connectionId=$CONNECTION_ID&commentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-comment?${params}`, {
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
| `commentId` | string | yes | ID of the comment to return. |

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
          "comment": "string",
          "commentOn": "string",
          "commentOnDocumentId": "string",
          "docketId": "string",
          "documentType": "string",
          "objectId": "string",
          "postedDate": "2026-05-07T12:00:00.000Z",
          "receiveDate": "2026-05-07T12:00:00.000Z",
          "subtype": "string",
          "title": "string",
          "trackingNbr": "string",
          "withdrawn": true
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
| `data` | object | Comment resource. |
| `data.attributes.agencyId` | string |  |
| `data.attributes.comment` | string |  |
| `data.attributes.commentOn` | string |  |
| `data.attributes.commentOnDocumentId` | string |  |
| `data.attributes.docketId` | string |  |
| `data.attributes.documentType` | string |  |
| `data.attributes.objectId` | string |  |
| `data.attributes.postedDate` | date |  |
| `data.attributes.receiveDate` | date |  |
| `data.attributes.subtype` | string |  |
| `data.attributes.title` | string |  |
| `data.attributes.trackingNbr` | string |  |
| `data.attributes.withdrawn` | boolean |  |
| `data.id` | string | Comment ID. |
| `data.links.self` | string |  |
| `data.relationships.attachments.links.related` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native GSA Public Comment API, this operation is `GET /comments/:commentId` (base URL `https://api.regulations.gov/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

