# DataForSEO: Get Keyword Ideas

Retrieves keyword idea data from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keyword-ideas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keyword-ideas?connectionId=$CONNECTION_ID&limit=25&offset=0&keywords%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "keywords[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keyword-ideas?${params}`, {
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
| `keywords[]` | array<string> | yes | Seed keywords used to generate new keyword ideas. |
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
      "avgBacklinksInfo": {},
      "keyword": "string",
      "keywordInfo": {},
      "keywordProperties": {},
      "languageCode": "string",
      "locationCode": 1,
      "searchIntentInfo": {},
      "seType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgBacklinksInfo` | object | Average backlink metrics for ranking pages when available. |
| `keyword` | string | Suggested keyword returned by DataForSEO. |
| `keywordInfo` | object | Keyword metrics such as search volume and competition. |
| `keywordProperties` | object | Additional keyword properties returned by the provider. |
| `languageCode` | string | Provider language code used for the keyword idea. |
| `locationCode` | number | Provider location code used for the keyword idea. |
| `searchIntentInfo` | object | Search intent classification returned for the keyword. |
| `seType` | string | Search engine type for the keyword-ideas record. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/google/keyword_ideas/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-keyword-ideas.md) for the provider-specific parameters and requirements.

