# Transifex: Update Project



```
PUT https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transifex/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The Transifex project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "ai_fillup": true,
        "archived": true,
        "datetime_created": "2026-05-07T12:00:00.000Z",
        "datetime_modified": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "homepage_url": "https://example.com",
        "instructions_url": "https://example.com",
        "license": "string",
        "logo_url": "https://example.com",
        "long_description": "string",
        "machine_translation_fillup": true,
        "name": "Ava Chen",
        "private": true,
        "repository_url": "https://example.com",
        "slug": "string",
        "translation_memory_fillup": true,
        "type": "string"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "relationships": {
        "languages": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "maintainers": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          },
          "links": {
            "related": "https://example.com"
          }
        },
        "resources": {
          "links": {
            "related": "https://example.com"
          }
        },
        "source_language": {
          "data": {
            "id": "string",
            "type": "string"
          },
          "links": {
            "related": "https://example.com"
          }
        },
        "team": {
          "data": {
            "id": "string",
            "type": "string"
          },
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
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
| `attributes.ai_fillup` | boolean |  |
| `attributes.archived` | boolean |  |
| `attributes.datetime_created` | date |  |
| `attributes.datetime_modified` | date |  |
| `attributes.description` | string |  |
| `attributes.homepage_url` | string |  |
| `attributes.instructions_url` | string |  |
| `attributes.license` | string |  |
| `attributes.logo_url` | string |  |
| `attributes.long_description` | string |  |
| `attributes.machine_translation_fillup` | boolean |  |
| `attributes.name` | string |  |
| `attributes.private` | boolean |  |
| `attributes.repository_url` | string |  |
| `attributes.slug` | string |  |
| `attributes.translation_memory_fillup` | boolean |  |
| `attributes.type` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `relationships.languages.links.related` | string |  |
| `relationships.languages.links.self` | string |  |
| `relationships.maintainers.links.related` | string |  |
| `relationships.maintainers.links.self` | string |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.organization.links.related` | string |  |
| `relationships.resources.links.related` | string |  |
| `relationships.source_language.data.id` | string |  |
| `relationships.source_language.data.type` | string |  |
| `relationships.source_language.links.related` | string |  |
| `relationships.team.data.id` | string |  |
| `relationships.team.data.type` | string |  |
| `relationships.team.links.related` | string |  |
| `relationships.team.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transifex API, this operation is `PATCH /projects/:project_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

