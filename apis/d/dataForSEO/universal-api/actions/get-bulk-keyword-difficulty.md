# DataForSEO: Get Bulk Keyword Difficulty

Retrieves bulk keyword difficulty from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-keyword-difficulty
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-keyword-difficulty?connectionId=$CONNECTION_ID&keywords%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keywords[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-keyword-difficulty?${params}`, {
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
| `keywords[]` | array<string> | yes | Keywords to score for difficulty in bulk. |
| `location_name` | string | no | Location context for the DataForSEO Labs analysis. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_code` | string | no | Language code for the analysis context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keyword": "string",
      "keywordDifficulty": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keyword` | string | Submitted keyword evaluated for ranking difficulty. |
| `keywordDifficulty` | number | Difficulty score returned by DataForSEO. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/bulk_keyword_difficulty/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-keyword-difficulty.md) for the provider-specific parameters and requirements.

