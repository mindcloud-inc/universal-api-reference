# Energy Information Administration: Query Crude Oil Imports Data

Retrieves crude oil import data from EIA.

```
GET https://connect.mindcloud.co/v1/universal/energyInformationAdministration/latest/actions/query-crude-oil-imports-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Energy Information Administration `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/energyInformationAdministration/latest/actions/query-crude-oil-imports-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/energyInformationAdministration/latest/actions/query-crude-oil-imports-data?${params}`, {
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
| `dataColumns` | string | no | One or more EIA data column IDs to return. Accepts multiple values as an array. |
| `frequency` | string | no | Optional EIA frequency code for the dataset, such as annual, monthly, daily, or hourly where supported. |
| `start` | string | no | Optional inclusive start period in the format supported by the selected EIA route. Example: `2024`. |
| `end` | string | no | Optional inclusive end period in the format supported by the selected EIA route. Example: `2025`. |
| `facetFiltersJson` | string | no | Optional JSON object mapping EIA facet IDs to one or more values. Example: {"stateid":["CA"]}. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Energy Information Administration API returns.

## Native endpoint

Through the native Energy Information Administration API, this operation is `GET /crude-oil-imports/data` (base URL `https://api.eia.gov/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-crude-oil-imports-data.md) for the provider-specific parameters and requirements.

