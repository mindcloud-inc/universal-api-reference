# Rat Genome Database: Search Pathways



```
GET https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/search-pathways
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rat Genome Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/search-pathways?connectionId=$CONNECTION_ID&searchString=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchString": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ratGenomeDatabase/latest/actions/search-pathways?${params}`, {
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
| `searchString` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "hasAlteredPath": "string",
      "id": "string",
      "name": "Ava Chen",
      "objectList": [
        {}
      ],
      "pathwayCategories": [
        "string"
      ],
      "referenceList": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Pathway description. |
| `hasAlteredPath` | string | Whether an altered pathway is available. |
| `id` | string | Pathway accession identifier. |
| `name` | string | Pathway name. |
| `objectList` | array<object> | Related object list when available. |
| `pathwayCategories` | array<string> | Pathway category labels. |
| `referenceList` | array<object> | Reference list when available. |

## Native endpoint

Through the native Rat Genome Database API, this operation is `GET /pathways/diagrams/search/:searchString` (base URL `https://rest.rgd.mcw.edu/rgdws`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-pathways.md) for the provider-specific parameters and requirements.

