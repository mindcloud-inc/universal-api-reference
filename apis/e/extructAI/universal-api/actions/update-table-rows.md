# Extruct AI: Update Table Rows

Updates table rows in Extruct AI.

```
PUT https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/update-table-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/update-table-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string",
  "rows[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/update-table-rows', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string",
    "rows[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | Target table identifier. |
| `rows[]` | array<object> | yes | Array of row update objects; each requires `data` and can include `id` for the target row. |
| `run` | boolean | no | Whether to run the table after updating rows. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_profile_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "id": "string",
      "metadata": {},
      "parent_data": {},
      "parent_row_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_profile_id` | string |  |
| `created_at` | date |  |
| `data` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `parent_data` | object |  |
| `parent_row_id` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `PATCH /v1/tables/:table_id/rows` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-table-rows.md) for the provider-specific parameters and requirements.

