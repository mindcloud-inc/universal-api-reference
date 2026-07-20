# Transifex: Get Resource



```
GET https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-resource?connectionId=$CONNECTION_ID&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-resource?${params}`, {
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
| `resourceId` | string | yes | The Transifex resource identifier. |

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

Through the native Transifex API, this operation is `GET /resources/:resource_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

