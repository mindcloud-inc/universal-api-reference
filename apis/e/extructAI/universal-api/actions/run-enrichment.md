# Extruct AI: Run Enrichment

Runs enrichment on a table in Extruct AI.

```
POST https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/run-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/run-enrichment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/run-enrichment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | Target table identifier. |
| `mode` | string | no | Defaults to new. Allowed values: new, all, failed. One of: `0`, `1`, `2`. Default: `new`. |
| `rows[]` | array<string> | no | Optional row IDs to scope the run. |
| `columns[]` | array<string> | no | Optional column IDs to scope the run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        "string"
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "mode": "string",
      "num_requested_cells": 1,
      "rows": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<string> |  |
| `created_at` | date |  |
| `id` | string |  |
| `mode` | string |  |
| `num_requested_cells` | number |  |
| `rows` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `POST /v1/tables/:table_id/run` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-enrichment.md) for the provider-specific parameters and requirements.

