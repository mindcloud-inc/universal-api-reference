# GrowthBook: Bulk import fact tables, filters, and metrics

Bulk imports fact tables, filters, and metrics into GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-bulk-import-facts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-bulk-import-facts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-bulk-import-facts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `factTables[]` | array<object> | no |  |
| `factTableFilters[]` | array<object> | no |  |
| `factMetrics[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "factMetricsAdded": 1,
      "factMetricsUpdated": 1,
      "factTableFiltersAdded": 1,
      "factTableFiltersUpdated": 1,
      "factTablesAdded": 1,
      "factTablesUpdated": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `factMetricsAdded` | number |  |
| `factMetricsUpdated` | number |  |
| `factTableFiltersAdded` | number |  |
| `factTableFiltersUpdated` | number |  |
| `factTablesAdded` | number |  |
| `factTablesUpdated` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /bulk-import/facts` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-bulk-import-facts.md) for the provider-specific parameters and requirements.

