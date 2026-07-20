# DataForSEO: Get Domain Rank Overview

Retrieves domain rank overview data from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-domain-rank-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-domain-rank-overview?connectionId=$CONNECTION_ID&target=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-domain-rank-overview?${params}`, {
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
| `target` | string | yes | Domain to analyze for rank overview. |
| `location_name` | string | no | Location context for the DataForSEO Labs analysis. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_code` | string | no | Language code for the analysis context. |
| `ignore_synonyms` | boolean | no | Exclude synonymous keywords from the overview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "languageCode": "string",
      "locationCode": 1,
      "metrics": {},
      "seType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `languageCode` | string | Provider language code used for the overview. |
| `locationCode` | number | Provider location code used for the overview. |
| `metrics` | object | Aggregated ranking metrics for the requested domain. |
| `seType` | string | Search engine type for the domain overview record. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/google/domain_rank_overview/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-rank-overview.md) for the provider-specific parameters and requirements.

