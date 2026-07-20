# DataForSEO: Get Competitor Domains

Retrieves competitor domain data from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-competitor-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-competitor-domains?connectionId=$CONNECTION_ID&limit=25&offset=0&target=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "target": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-competitor-domains?${params}`, {
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
| `target` | string | yes | Domain to analyze for competing domains. |
| `location_name` | string | no | Location context for the DataForSEO Labs analysis. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_code` | string | no | Language code for the analysis context. |
| `ignore_synonyms` | boolean | no | Exclude synonymous keywords from the comparison. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avgPosition": 1,
      "competitorMetrics": {},
      "domain": "string",
      "fullDomainMetrics": {},
      "intersections": 1,
      "metrics": {},
      "seType": "string",
      "sumPosition": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avgPosition` | number | Average ranking position across intersecting keywords. |
| `competitorMetrics` | object | Comparative metrics describing overlap with the target domain. |
| `domain` | string | Competing domain returned for the requested target. |
| `fullDomainMetrics` | object | Aggregated metrics for the full competing domain. |
| `intersections` | number | Count of shared ranking keywords between the target and competitor. |
| `metrics` | object | Keyword and traffic metrics for the competing domain. |
| `seType` | string | Search engine type for the competitor-domain record. |
| `sumPosition` | number | Summed ranking position across intersecting keywords. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/google/competitors_domain/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-competitor-domains.md) for the provider-specific parameters and requirements.

