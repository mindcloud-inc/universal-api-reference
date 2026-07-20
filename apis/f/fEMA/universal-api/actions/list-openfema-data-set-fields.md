# FEMA: List OpenFEMA Data Set Fields

Retrieves OpenFEMA data set fields from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-openfema-data-set-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-openfema-data-set-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-openfema-data-set-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "datasetId": "string",
      "datasetVersion": 1,
      "description": "string",
      "hash": "string",
      "id": "string",
      "isNestedObject": true,
      "isNullable": true,
      "isSearchable": true,
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "openFemaDataSet": "string",
      "primaryKey": true,
      "sortOrder": 1,
      "srid": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasetId` | string |  |
| `datasetVersion` | number |  |
| `description` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `isNestedObject` | boolean |  |
| `isNullable` | boolean |  |
| `isSearchable` | boolean |  |
| `lastRefresh` | date |  |
| `name` | string |  |
| `openFemaDataSet` | string |  |
| `primaryKey` | boolean |  |
| `sortOrder` | number |  |
| `srid` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/DataSetFields` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-openfema-data-set-fields.md) for the provider-specific parameters and requirements.

