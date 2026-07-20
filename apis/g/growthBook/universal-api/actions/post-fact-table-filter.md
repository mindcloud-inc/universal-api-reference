# GrowthBook: Create a single fact table filter

Creates a fact table filter in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-table-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-table-filter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "factTableId": "fact_table_1",
  "name": "sample",
  "value": "sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/post-fact-table-filter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "factTableId": "fact_table_1",
    "name": "sample",
    "value": "sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `factTableId` | string | yes | Specify a specific fact table Default: `fact_table_1`. |
| `name` | string | yes | Default: `sample`. |
| `description` | string | no | Description of the fact table filter |
| `value` | string | yes | The SQL expression for this filter. Default: `sample`. |
| `managedBy` | string | no | Set this to "api" to disable editing in the GrowthBook UI. Before you do this, the Fact Table itself must also be marked as "api" |

## Response

```json
{
  "success": true,
  "data": [
    {
      "factTableFilter": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `factTableFilter` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /fact-tables/:factTableId/filters` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-fact-table-filter.md) for the provider-specific parameters and requirements.

