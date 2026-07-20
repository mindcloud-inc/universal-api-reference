# Transifex: Get Resource String



```
GET https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-resource-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-resource-string?connectionId=$CONNECTION_ID&resourceStringId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceStringId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-resource-string?${params}`, {
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
| `resourceStringId` | string | yes | The Transifex resource string identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "appearance_order": 1,
        "context": "string",
        "datetime_created": "2026-05-07T12:00:00.000Z",
        "key": "string",
        "metadata_datetime_modified": "2026-05-07T12:00:00.000Z",
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
| `attributes.context` | string |  |
| `attributes.datetime_created` | date |  |
| `attributes.key` | string |  |
| `attributes.metadata_datetime_modified` | date |  |
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

Through the native Transifex API, this operation is `GET /resource_strings/:resource_string_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource-string.md) for the provider-specific parameters and requirements.

