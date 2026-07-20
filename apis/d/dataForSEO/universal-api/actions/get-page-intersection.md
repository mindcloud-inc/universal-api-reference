# DataForSEO: Get Page Intersection

Retrieves page intersection data from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-page-intersection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-page-intersection?connectionId=$CONNECTION_ID&limit=25&offset=0&pages=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "pages": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-page-intersection?${params}`, {
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
| `pages` | object | yes | Object containing the pages to compare, keyed by numeric identifiers such as 1 and 2. |
| `location_name` | string | no | Location context for the DataForSEO Labs analysis. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_code` | string | no | Language code for the analysis context. |
| `intersection_mode` | list<string> | no | How the page sets should be combined for comparison. One of: `intersect`, `union`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "intersectionResult": {},
      "keywordData": {},
      "seType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `intersectionResult` | object | Comparison object describing how the submitted pages intersect for the keyword. |
| `keywordData` | object | Keyword descriptor object for the shared ranking term. |
| `seType` | string | Search engine type for the page-intersection record. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/google/page_intersection/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-page-intersection.md) for the provider-specific parameters and requirements.

