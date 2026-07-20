# Transifex: Create Resource



```
POST https://connect.mindcloud.co/v1/universal/transifex/latest/actions/create-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/create-resource" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transifex/latest/actions/create-resource', {
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
        "accept_translations": true,
        "datetime_created": "2026-05-07T12:00:00.000Z",
        "datetime_modified": "2026-05-07T12:00:00.000Z",
        "i18n_type": "string",
        "i18n_version": 1,
        "name": "Ava Chen",
        "priority": "string",
        "slug": "string",
        "string_count": 1,
        "word_count": 1
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "relationships": {
        "i18n_format": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "project": {
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
| `attributes.accept_translations` | boolean |  |
| `attributes.datetime_created` | date |  |
| `attributes.datetime_modified` | date |  |
| `attributes.i18n_type` | string |  |
| `attributes.i18n_version` | number |  |
| `attributes.name` | string |  |
| `attributes.priority` | string |  |
| `attributes.slug` | string |  |
| `attributes.string_count` | number |  |
| `attributes.word_count` | number |  |
| `id` | string |  |
| `links.self` | string |  |
| `relationships.i18n_format.data.id` | string |  |
| `relationships.i18n_format.data.type` | string |  |
| `relationships.project.data.id` | string |  |
| `relationships.project.data.type` | string |  |
| `relationships.project.links.related` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transifex API, this operation is `POST /resources` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-resource.md) for the provider-specific parameters and requirements.

