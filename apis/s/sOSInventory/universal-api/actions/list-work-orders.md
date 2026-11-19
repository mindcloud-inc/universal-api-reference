# SOS Inventory: List Work Orders



```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-work-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-work-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-work-orders?${params}`, {
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
| `query` | string | no | Match work order number, customer, or comments. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | list<string> | no | One of: `closed`, `open`. |
| `archived` | list<string> | no | One of: `no`, `yes`. |
| `from` | date | no | Example: `2026-01-01T00:00:00`. |
| `to` | date | no | Example: `2026-01-01T00:00:00`. |
| `createdSince` | date | no | Example: `2026-01-01T00:00:00`. |
| `updatedSince` | date | no | Example: `2026-01-01T00:00:00`. |
| `summary` | string | no | Any supplied value returns summary fields only. Leave empty for complete records. Example: `yes`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "closed": true,
      "comment": "string",
      "customerNotes": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "hasSignature": true,
      "id": 1,
      "lines": [
        {
          "altAmount": 1,
          "amount": 1,
          "backOrdered": 1,
          "class": {
            "id": 1,
            "name": "Ava Chen"
          },
          "description": "string",
          "duedate": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "invoiced": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "lineNumber": 1,
          "picked": 1,
          "produced": 1,
          "quantity": 1,
          "returned": 1,
          "shipped": 1,
          "unitprice": 1,
          "volume": 1,
          "volumeunit": "string",
          "weight": 1,
          "weightunit": "string"
        }
      ],
      "location": {
        "id": 1,
        "name": "Ava Chen"
      },
      "number": "string",
      "starred": 1,
      "summaryOnly": true,
      "syncToken": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `closed` | boolean |  |
| `comment` | string |  |
| `customerNotes` | string |  |
| `date` | date |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `lines` | array<object> |  |
| `lines[].altAmount` | number |  |
| `lines[].amount` | number |  |
| `lines[].backOrdered` | number |  |
| `lines[].class.id` | number |  |
| `lines[].class.name` | string |  |
| `lines[].description` | string |  |
| `lines[].duedate` | date |  |
| `lines[].id` | number |  |
| `lines[].invoiced` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].lineNumber` | number |  |
| `lines[].picked` | number |  |
| `lines[].produced` | number |  |
| `lines[].quantity` | number |  |
| `lines[].returned` | number |  |
| `lines[].shipped` | number |  |
| `lines[].unitprice` | number |  |
| `lines[].volume` | number |  |
| `lines[].volumeunit` | string |  |
| `lines[].weight` | number |  |
| `lines[].weightunit` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `number` | string |  |
| `starred` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |
| `total` | number |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/workorder` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-orders.md) for the provider-specific parameters and requirements.

