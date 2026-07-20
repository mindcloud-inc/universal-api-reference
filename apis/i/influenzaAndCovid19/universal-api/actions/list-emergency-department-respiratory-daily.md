# Influenza and Covid-19: List Emergency Department Respiratory Daily



```
GET https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-respiratory-daily
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influenza and Covid-19 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-respiratory-daily?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-respiratory-daily?${params}`, {
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
| `date` | date | no | Filter to an exact CDC date timestamp, for example 2022-09-25T00:00:00.000. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `where` | string | no | Optional advanced SoQL where clause for CDC Data.CDC.gov filtering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "geography": "string",
      "pathogen": "string",
      "percent_visits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | CDC observation date. |
| `geography` | string | Geographic area reported by CDC. |
| `pathogen` | string | Respiratory pathogen or illness category. |
| `percent_visits` | number | Percentage of emergency department visits. |

## Native endpoint

Through the native Influenza and Covid-19 API, this operation is `GET /resource/vjzj-u7u8.json` (base URL `https://data.cdc.gov`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-emergency-department-respiratory-daily.md) for the provider-specific parameters and requirements.

