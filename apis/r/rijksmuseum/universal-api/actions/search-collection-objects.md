# Rijksmuseum: Search Collection Objects



```
GET https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/search-collection-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rijksmuseum `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/search-collection-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/search-collection-objects?${params}`, {
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
| `title` | string | no | Search for objects by title, such as Night Watch. |
| `creator` | string | no | Search for objects by creator name, such as Rembrandt van Rijn. |
| `objectNumber` | string | no | Search by Rijksmuseum object number. Supports wildcards, such as SK-C-5*. |
| `type` | string | no | Search by object type, such as painting. |
| `material` | string | no | Search by material, such as canvas or oil paint. |
| `technique` | string | no | Search by technique used to create the object. |
| `description` | string | no | Search keywords present in object descriptions. |
| `imageAvailable` | boolean | no | Filter objects by whether a digital reproduction is available. |
| `creationDate` | string | no | Search by year or wildcard period, such as 1642 or 16??. |
| `aboutActor` | string | no | Search for objects depicting or about a person or group by name. |
| `memberOfSetId` | string | no | Search for objects that are part of a Rijksmuseum set identifier URL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageToken` | string | no | Token from the previous search response next.id URL for pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "id": "string",
      "next": {},
      "orderedItems": [
        {}
      ],
      "partOf": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `id` | string |  |
| `next` | object |  |
| `orderedItems` | array<object> |  |
| `partOf` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Rijksmuseum API, this operation is `GET /search/collection` (base URL `https://data.rijksmuseum.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-collection-objects.md) for the provider-specific parameters and requirements.

