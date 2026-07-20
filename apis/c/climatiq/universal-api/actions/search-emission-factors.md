# Climatiq: Search Emission Factors

Finds emission factors in Climatiq by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/search-emission-factors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climatiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/search-emission-factors?connectionId=$CONNECTION_ID&dataVersion=%5E33" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataVersion": "^33"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climatiq/latest/actions/search-emission-factors?${params}`, {
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
| `dataVersion` | string | yes | Required Climatiq data version, such as ^33. Example: `^33`. |
| `query` | string | no | Free-text emission factor search query. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `region` | string | no | Region code filter, such as GB or US-CA. |
| `year` | number | no | Emission factor year filter. |
| `category` | string | no | Emission factor category filter. |
| `unitType` | string | no | Unit type filter, such as Energy, Money, Weight, or Distance. |
| `scope` | string | no | GHG Protocol scope filter, such as 1, 2, 3, or 3.1. |
| `calculationMethod` | string | no | Calculation method filter: ar4, ar5, or ar6. |
| `accessType` | string | no | Emission factor access type: public, private, or premium. |
| `page` | number | no | Results page number. Climatiq defaults to 1. Default: `1`. |
| `resultsPerPage` | number | no | Number of results per page. Climatiq maximum is 500. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "last_page": 1,
      "notices": [
        {}
      ],
      "possible_filters": {},
      "results": [
        {}
      ],
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number | Current result page. |
| `last_page` | number | Last available result page. |
| `notices` | array<object> | Notices returned with the search result. |
| `possible_filters` | object | Filter values available for the current search. |
| `results` | array<object> | Emission factor results for this page. |
| `total_results` | number | Total matching emission factors. |

## Native endpoint

Through the native Climatiq API, this operation is `GET /data/v1/search` (base URL `https://api.climatiq.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-emission-factors.md) for the provider-specific parameters and requirements.

