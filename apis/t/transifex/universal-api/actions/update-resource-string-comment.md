# Transifex: Update Resource String Comment



```
PUT https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-resource-string-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-resource-string-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "commentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-resource-string-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "commentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "datetime_created": "2026-05-07T12:00:00.000Z",
        "datetime_modified": "2026-05-07T12:00:00.000Z",
        "message": "string",
        "priority": "string",
        "status": "string",
        "type": "string"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "relationships": {
        "author": {
          "data": {
            "id": "string",
            "type": "string"
          },
          "links": {
            "related": "https://example.com"
          }
        },
        "language": {
          "data": {
            "id": "string",
            "type": "string"
          },
          "links": {
            "related": "https://example.com"
          }
        },
        "resource_string": {
          "data": {
            "id": "string",
            "type": "string"
          },
          "links": {
            "related": "https://example.com"
          }
        },
        "resource": {
          "data": {
            "id": "string",
            "type": "string"
          },
          "links": {
            "related": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.datetime_created` | date |  |
| `attributes.datetime_modified` | date |  |
| `attributes.message` | string |  |
| `attributes.priority` | string |  |
| `attributes.status` | string |  |
| `attributes.type` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `relationships.author.data.id` | string |  |
| `relationships.author.data.type` | string |  |
| `relationships.author.links.related` | string |  |
| `relationships.language.data.id` | string |  |
| `relationships.language.data.type` | string |  |
| `relationships.language.links.related` | string |  |
| `relationships.resource_string.data.id` | string |  |
| `relationships.resource_string.data.type` | string |  |
| `relationships.resource_string.links.related` | string |  |
| `relationships.resource.data.id` | string |  |
| `relationships.resource.data.type` | string |  |
| `relationships.resource.links.related` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transifex API, this operation is `PATCH /resource_string_comments/:comment_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-resource-string-comment.md) for the provider-specific parameters and requirements.

