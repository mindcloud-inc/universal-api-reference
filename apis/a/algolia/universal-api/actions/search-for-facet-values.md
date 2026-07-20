# Algolia: Search for Facet Values

Searches facet values in an Algolia index.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-for-facet-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-for-facet-values?connectionId=$CONNECTION_ID&indexName=Ava%20Chen&facetName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen",
  "facetName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-for-facet-values?${params}`, {
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
| `indexName` | string | yes | The name of the Algolia index. |
| `facetName` | string | yes | The searchable facet attribute to query. |
| `facetQuery` | string | no | Text to search inside the facet values. |
| `maxFacetHits` | number | no | Maximum number of facet values to return. Default: `10`. |
| `params` | string | no | URL-encoded search parameters to apply while searching facet values. Example: `hitsPerPage=5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exhaustiveFacetsCount": true,
      "facetHits": [
        {}
      ],
      "processingTimeMS": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exhaustiveFacetsCount` | boolean |  |
| `facetHits` | array<object> |  |
| `processingTimeMS` | number |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/facets/:facetName/query` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-for-facet-values.md) for the provider-specific parameters and requirements.

