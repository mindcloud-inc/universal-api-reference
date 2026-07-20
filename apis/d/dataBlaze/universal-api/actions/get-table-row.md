# Data Blaze: Get Table Row

Retrieves a table row from Data Blaze.

```
GET https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/get-table-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/get-table-row?connectionId=$CONNECTION_ID&rowId=43iv2oFvcdRKAHpnf1RKdE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowId": "43iv2oFvcdRKAHpnf1RKdE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/get-table-row?${params}`, {
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
| `rowId` | string | yes | Mindcloud row ID. Example: `43iv2oFvcdRKAHpnf1RKdE`. |

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
| `id` | string | Data Blaze row ID. |
| `order` | string | Data Blaze row order token. |

## Native endpoint

Through the native Data Blaze API, this operation is `GET /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/{rowId}/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-row.md) for the provider-specific parameters and requirements.

