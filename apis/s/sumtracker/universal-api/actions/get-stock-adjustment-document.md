# Sumtracker: Get Stock Adjustment Document

Retrieves a stock adjustment document from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-stock-adjustment-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-stock-adjustment-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-stock-adjustment-document?${params}`, {
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
| `id` | string | yes | Stock adjustment document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number": "string",
      "adjustmentType": "string",
      "actionPerformed": "string",
      "isComplete": true,
      "isTaskInProgress": true,
      "created": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z",
      "totalQuantity": 1,
      "notes": "string",
      "id": 1,
      "warehouseId": 1,
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | string |  |
| `adjustmentType` | string |  |
| `actionPerformed` | string |  |
| `isComplete` | boolean |  |
| `isTaskInProgress` | boolean |  |
| `created` | date |  |
| `updated` | date |  |
| `totalQuantity` | number |  |
| `notes` | string |  |
| `id` | number |  |
| `warehouseId` | number |  |
| `reason` | string |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/stock/adjustment/documents/:id/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock-adjustment-document.md) for the provider-specific parameters and requirements.

