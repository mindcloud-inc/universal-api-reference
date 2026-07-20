# DataForSEO: Get Keyword Overview

Retrieves keyword overview data from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keyword-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keyword-overview?connectionId=$CONNECTION_ID&keywords%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keywords[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-keyword-overview?${params}`, {
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
| `keywords[]` | array<string> | yes | Keywords to summarize in the overview response. |
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
| `keyword` | string | Keyword returned in the overview response. |
| `keywordInfo` | object | Keyword metrics such as search volume and competition. |
| `keywordProperties` | object | Additional keyword properties returned by the provider. |
| `languageCode` | string | Provider language code used for the overview. |
| `locationCode` | number | Provider location code used for the overview. |
| `searchIntentInfo` | object | Search intent classification returned for the keyword. |
| `seType` | string | Search engine type for the keyword-overview record. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/google/keyword_overview/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keyword-overview.md) for the provider-specific parameters and requirements.

