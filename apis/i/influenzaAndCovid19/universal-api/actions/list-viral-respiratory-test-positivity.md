# Influenza and Covid-19: List Viral Respiratory Test Positivity



```
GET https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-viral-respiratory-test-positivity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influenza and Covid-19 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-viral-respiratory-test-positivity?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-viral-respiratory-test-positivity?${params}`, {
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
| `pathogen` | string | no | Filter to a CDC pathogen value, such as COVID-19, Influenza, or RSV. |
| `weekEnd` | date | no | Filter to an exact CDC week ending timestamp, for example 2022-10-01T00:00:00.000. |

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
      "pathogen": "string",
      "percent_test_positivity": 1,
      "week_end": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pathogen` | string | Respiratory pathogen. |
| `percent_test_positivity` | number | Percent of tests positive for the pathogen. |
| `week_end` | date | CDC week ending date. |

## Native endpoint

Through the native Influenza and Covid-19 API, this operation is `GET /resource/seuz-s2cv.json` (base URL `https://data.cdc.gov`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-viral-respiratory-test-positivity.md) for the provider-specific parameters and requirements.

