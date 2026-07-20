# Data Blaze: Update Table Row

Updates an existing table row in Data Blaze.

```
PUT https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/update-table-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/update-table-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rowId": "43iv2oFvcdRKAHpnf1RKdE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/update-table-row', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rowId": "43iv2oFvcdRKAHpnf1RKdE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rowId` | string | yes | Mindcloud row ID. Example: `43iv2oFvcdRKAHpnf1RKdE`. |
| `name` | string | no | Updated value for the Mindcloud Name field. Example: `Jane Doe`. |
| `count` | number | no | Updated value for the Mindcloud Count field. Example: `42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_028bLj7zLab3TYslzthhXu": "string",
      "field_2Te3k3Sf4edLQ3a0WE2a8J": "string",
      "id": "string",
      "order": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_028bLj7zLab3TYslzthhXu` | string | Updated Mindcloud Name field value. |
| `field_2Te3k3Sf4edLQ3a0WE2a8J` | string | Updated Mindcloud Count field value returned by Data Blaze. |
| `id` | string | Updated Data Blaze row ID. |
| `order` | string | Updated row order token. |

## Native endpoint

Through the native Data Blaze API, this operation is `PATCH /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-table-row.md) for the provider-specific parameters and requirements.

