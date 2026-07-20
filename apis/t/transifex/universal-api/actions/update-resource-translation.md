# Transifex: Update Resource Translation



```
PUT https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-resource-translation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-resource-translation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceTranslationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-resource-translation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceTranslationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceTranslationId` | string | yes | The Transifex resource translation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "datetime_created": "2026-05-07T12:00:00.000Z",
        "datetime_translated": "2026-05-07T12:00:00.000Z",
        "finalized": true,
        "origin": "string",
        "proofread": true,
        "reviewed": true,
        "strings": {
          "other": "string"
        }
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "relationships": {
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
        },
        "translator": {
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
| `attributes.datetime_translated` | date |  |
| `attributes.finalized` | boolean |  |
| `attributes.origin` | string |  |
| `attributes.proofread` | boolean |  |
| `attributes.reviewed` | boolean |  |
| `attributes.strings.other` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `relationships.language.data.id` | string |  |
| `relationships.language.data.type` | string |  |
| `relationships.language.links.related` | string |  |
| `relationships.resource_string.data.id` | string |  |
| `relationships.resource_string.data.type` | string |  |
| `relationships.resource_string.links.related` | string |  |
| `relationships.resource.data.id` | string |  |
| `relationships.resource.data.type` | string |  |
| `relationships.resource.links.related` | string |  |
| `relationships.translator.data.id` | string |  |
| `relationships.translator.data.type` | string |  |
| `relationships.translator.links.related` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transifex API, this operation is `PATCH /resource_translations/:resource_translation_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-resource-translation.md) for the provider-specific parameters and requirements.

