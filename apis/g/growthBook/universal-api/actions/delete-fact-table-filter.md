# GrowthBook: Deletes a single fact table filter

Deletes a fact table filter from GrowthBook.

```
DELETE https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-fact-table-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-fact-table-filter?connectionId=$CONNECTION_ID&factTableId=fact_table_1&id=prj_19g6smo332up7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "factTableId": "fact_table_1",
  "id": "prj_19g6smo332up7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/delete-fact-table-filter?${params}`, {
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
| `factTableId` | string | yes | Specify a specific fact table Default: `fact_table_1`. |
| `id` | string | yes | The id of the requested resource Default: `prj_19g6smo332up7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedId` | string | The ID of the deleted fact filter |

## Native endpoint

Through the native GrowthBook API, this operation is `DELETE /fact-tables/:factTableId/filters/:id` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-fact-table-filter.md) for the provider-specific parameters and requirements.

