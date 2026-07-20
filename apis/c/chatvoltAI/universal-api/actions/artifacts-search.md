# Chatvolt AI: Search Artifacts

Searches artifacts in Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-search?${params}`, {
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
| `q` | string | no | Search term for name, description, or category name. Ignored if `ids` is present. |
| `ids[]` | array<string> | no | List of specific Artifact IDs (e.g., `id1,id2`). Overrides textual search. |
| `minPrice` | number | no | Minimum price filter. |
| `maxPrice` | number | no | Maximum price filter. |
| `categoryIds[]` | array<string> | no | List of category IDs. Includes sub-categories automatically. |
| `mediaTypes[]` | array<string> | no | Filter by media types (e.g., `IMAGE,VIDEO`). |
| `maxMedias` | number | no | Max number of media items to return per artifact. |
| `includeInactive` | boolean | no | If true, returns inactive artifacts as well. |
| `limit` | number | no | Pagination limit. |
| `page` | number | no | Pagination page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array | Data. |
| `meta` | object | Meta. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /artifacts/search` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/artifacts-search.md) for the provider-specific parameters and requirements.

