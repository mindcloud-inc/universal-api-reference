# Data Blaze: Move Table Row

Moves a table row in Data Blaze.

```
PUT https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/move-table-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/move-table-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "rowId": "43iv2oFvcdRKAHpnf1RKdE",
  "beforeId": "3eHhgNuM5c4cZ6tRwbYVAs"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/move-table-row', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "rowId": "43iv2oFvcdRKAHpnf1RKdE",
    "beforeId": "3eHhgNuM5c4cZ6tRwbYVAs"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rowId` | string | yes | Mindcloud row ID to move. Example: `43iv2oFvcdRKAHpnf1RKdE`. |
| `beforeId` | string | yes | Move the row before this existing row ID. Example: `3eHhgNuM5c4cZ6tRwbYVAs`. |

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
| `field_028bLj7zLab3TYslzthhXu` | string | Mindcloud Name field value. |
| `field_2Te3k3Sf4edLQ3a0WE2a8J` | string | Mindcloud Count field value returned by Data Blaze. |
| `id` | string | Moved Data Blaze row ID. |
| `order` | string | Moved row order token after reordering. |

## Native endpoint

Through the native Data Blaze API, this operation is `PATCH /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/move/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-table-row.md) for the provider-specific parameters and requirements.

