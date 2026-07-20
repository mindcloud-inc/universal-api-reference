# Data Blaze: Create Table Row

Creates a new table row in Data Blaze.

```
POST https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/create-table-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data Blaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/create-table-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Jane Doe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataBlaze/latest/actions/create-table-row', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Jane Doe"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Value for the Mindcloud Name field. Example: `Jane Doe`. |
| `count` | number | no | Value for the Mindcloud Count field. Example: `42`. |

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
| `field_028bLj7zLab3TYslzthhXu` | string | Created Mindcloud Name field value. |
| `field_2Te3k3Sf4edLQ3a0WE2a8J` | string | Created Mindcloud Count field value returned by Data Blaze. |
| `id` | string | Created Data Blaze row ID. |
| `order` | string | Created row order token. |

## Native endpoint

Through the native Data Blaze API, this operation is `POST /api/database/rows/table/6S69TxVQg3kaNMphZCdHyV/` (base URL `https://data-api.blaze.today`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-table-row.md) for the provider-specific parameters and requirements.

