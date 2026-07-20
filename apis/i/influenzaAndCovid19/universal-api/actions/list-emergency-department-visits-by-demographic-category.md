# Influenza and Covid-19: List Emergency Department Visits by Demographic Category



```
GET https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-visits-by-demographic-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influenza and Covid-19 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-visits-by-demographic-category?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-visits-by-demographic-category?${params}`, {
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
| `pathogen` | string | no | Filter to a CDC pathogen value such as COVID-19, Influenza, RSV, Combined, or ARI. |
| `geography` | string | no | Filter to a geography value in the CDC dataset, such as United States or a state name. |
| `demographicsType` | string | no | Filter to the demographic category type reported by CDC, such as Age Group or Sex. |
| `demographicsValue` | string | no | Filter to a specific demographic value reported by CDC, such as 50-64 years. |
| `weekEnd` | date | no | Filter to an exact CDC week ending timestamp, for example 2026-04-18T00:00:00.000. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `where` | string | no | Optional advanced SoQL where clause for CDC Data.CDC.gov filtering when exact-match fields are not enough. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "demographics_type": "string",
      "demographics_values": "string",
      "geography": "string",
      "pathogen": "string",
      "percent_visits": 1,
      "week_end": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `demographics_type` | string | Demographic category type. |
| `demographics_values` | string | Demographic value. |
| `geography` | string | Geographic area reported by CDC. |
| `pathogen` | string | Respiratory pathogen or combined respiratory illness category. |
| `percent_visits` | number | Percentage of emergency department visits. |
| `week_end` | date | CDC week ending date. |

## Native endpoint

Through the native Influenza and Covid-19 API, this operation is `GET /resource/7xva-uux8.json` (base URL `https://data.cdc.gov`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-emergency-department-visits-by-demographic-category.md) for the provider-specific parameters and requirements.

