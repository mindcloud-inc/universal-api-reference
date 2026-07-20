# Transifex: Create Resource String



```
POST https://connect.mindcloud.co/v1/universal/transifex/latest/actions/create-resource-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/create-resource-string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transifex/latest/actions/create-resource-string', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "appearance_order": 1,
        "character_limit": 1,
        "context": "string",
        "datetime_created": "2026-05-07T12:00:00.000Z",
        "developer_comment": "string",
        "instructions": "string",
        "key": "string",
        "metadata_datetime_modified": "2026-05-07T12:00:00.000Z",
        "occurrences": "string",
        "pluralized": true,
        "string_hash": "string",
        "strings_datetime_modified": "2026-05-07T12:00:00.000Z",
        "strings": {
          "one": "string",
          "other": "string"
        }
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "relationships": {
        "committer": {
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
| `attributes.appearance_order` | number |  |
| `attributes.character_limit` | number |  |
| `attributes.context` | string |  |
| `attributes.datetime_created` | date |  |
| `attributes.developer_comment` | string |  |
| `attributes.instructions` | string |  |
| `attributes.key` | string |  |
| `attributes.metadata_datetime_modified` | date |  |
| `attributes.occurrences` | string |  |
| `attributes.pluralized` | boolean |  |
| `attributes.string_hash` | string |  |
| `attributes.strings_datetime_modified` | date |  |
| `attributes.strings.one` | string |  |
| `attributes.strings.other` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `relationships.committer.data.id` | string |  |
| `relationships.committer.data.type` | string |  |
| `relationships.committer.links.related` | string |  |
| `relationships.language.data.id` | string |  |
| `relationships.language.data.type` | string |  |
| `relationships.language.links.related` | string |  |
| `relationships.resource.data.id` | string |  |
| `relationships.resource.data.type` | string |  |
| `relationships.resource.links.related` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transifex API, this operation is `POST /resource_strings` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-resource-string.md) for the provider-specific parameters and requirements.

