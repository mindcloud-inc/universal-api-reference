# DataForSEO: Get Keywords for Site

Retrieves keywords for a site from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keywords-for-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keywords-for-site?connectionId=$CONNECTION_ID&limit=25&offset=0&target=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "target": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keywords-for-site?${params}`, {
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
| `target` | string | yes | Domain to analyze for site keywords. |
| `location_name` | string | no | Location context for the DataForSEO Labs analysis. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_code` | string | no | Language code for the analysis context. |
| `include_subdomains` | boolean | no | Include subdomains of the target domain. |

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
| `keyword` | string | Keyword returned for the requested target site. |
| `keywordInfo` | object | Keyword metrics such as search volume and competition. |
| `keywordProperties` | object | Additional keyword properties returned by the provider. |
| `languageCode` | string | Provider language code used for the keyword record. |
| `locationCode` | number | Provider location code used for the keyword record. |
| `searchIntentInfo` | object | Search intent classification returned for the keyword. |
| `seType` | string | Search engine type for the keywords-for-site record. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/google/keywords_for_site/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-keywords-for-site.md) for the provider-specific parameters and requirements.

