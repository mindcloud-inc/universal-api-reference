# Data Blaze: Delete Table Row

Deletes an existing table row from Data Blaze.

```
DELETE https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/delete-table-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/delete-table-row?connectionId=$CONNECTION_ID&rowId=43iv2oFvcdRKAHpnf1RKdE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowId": "43iv2oFvcdRKAHpnf1RKdE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/delete-table-row?${params}`, {
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
| `rowId` | string | yes | Mindcloud row ID to delete. Example: `43iv2oFvcdRKAHpnf1RKdE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Deleted row ID when a client or mapper surfaces it; Data Blaze DELETE may otherwise return an empty success body. |

## Native endpoint

Through the native Data Blaze API, this operation is `DELETE /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-table-row.md) for the provider-specific parameters and requirements.

