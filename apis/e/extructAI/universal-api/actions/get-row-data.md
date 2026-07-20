# Extruct AI: Get Row Data

Retrieves table row data from Extruct AI.

```
GET https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-row-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-row-data?connectionId=$CONNECTION_ID&tableId=string&rowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string",
  "rowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-row-data?${params}`, {
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
| `tableId` | string | yes | Target table identifier. |
| `rowId` | string | yes | Target row identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        {}
      ],
      "company_profile_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "id": "string",
      "metadata": {},
      "parent_data": {},
      "parent_row_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | array<object> |  |
| `company_profile_id` | string |  |
| `created_at` | date |  |
| `data` | object |  |
| `id` | string |  |
| `metadata` | object |  |
| `parent_data` | object |  |
| `parent_row_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `GET /v1/tables/:table_id/rows/:row_id` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-row-data.md) for the provider-specific parameters and requirements.

