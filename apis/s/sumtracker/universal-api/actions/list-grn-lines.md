# Sumtracker: List Goods Receipt Note Lines

Retrieves goods receipt note lines from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-grn-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-grn-lines?connectionId=$CONNECTION_ID&limit=25&offset=0&document_type=string&grn_id=string&po_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "document_type": "string",
  "grn_id": "string",
  "po_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-grn-lines?${params}`, {
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
| `document_type` | string | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `grn_id` | string | yes | Goods receipt note ID. |
| `po_id` | string | yes | Purchase order or stock transfer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "isStockTransfer": true,
          "created": "2026-05-07T12:00:00.000Z",
          "quantity": 1,
          "lineSubtotal": "string",
          "lineTax": "string",
          "lineTotal": "string",
          "id": 1,
          "grnId": 1,
          "polineId": 1
        }
      ],
      "count": 1,
      "next": "string",
      "previous": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].isStockTransfer` | boolean |  |
| `results[].created` | date |  |
| `results[].quantity` | number |  |
| `results[].lineSubtotal` | string |  |
| `results[].lineTax` | string |  |
| `results[].lineTotal` | string |  |
| `results[].id` | number |  |
| `results[].grnId` | number |  |
| `results[].polineId` | number |  |
| `count` | number |  |
| `next` | string |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/purchases/:document_type/:po_id/grns/:grn_id/lines/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-grn-lines.md) for the provider-specific parameters and requirements.

