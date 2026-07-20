# Transifex: List Resource String Comments



```
GET https://connect.mindcloud.co/v1/universal/transifex/latest/actions/list-resource-string-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/list-resource-string-comments?connectionId=$CONNECTION_ID&filterOrganization=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filterOrganization": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transifex/latest/actions/list-resource-string-comments?${params}`, {
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
| `filterOrganization` | string | yes |  |
| `filterResourceString` | string | no |  |

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

Through the native Transifex API, this operation is `GET /resource_string_comments` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resource-string-comments.md) for the provider-specific parameters and requirements.

