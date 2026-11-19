# SOS Inventory: List Pick Tickets



```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-pick-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-pick-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-pick-tickets?${params}`, {
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
| `query` | string | no | Match pick ticket number, comment, customer, or location. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | list<string> | no | One of: `closed`, `open`. |
| `archived` | list<string> | no | One of: `no`, `yes`. |
| `from` | date | no | Example: `2026-01-01T00:00:00`. |
| `to` | date | no | Example: `2026-01-01T00:00:00`. |
| `location` | list<string> | no |  |
| `channel` | string | no |  |
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
      "assignedToUser": {
        "id": 1,
        "name": "Ava Chen"
      },
      "closed": true,
      "comment": "string",
      "customer": {
        "fullname": "Ava Chen",
        "id": 1,
        "name": "Ava Chen"
      },
      "date": "2026-05-07T12:00:00.000Z",
      "hasSignature": true,
      "id": 1,
      "lines": [
        {
          "altAmount": 1,
          "amount": 1,
          "backOrdered": 1,
          "description": "string",
          "duedate": "string",
          "id": 1,
          "invoiced": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "lineNumber": 1,
          "linkedTransaction": {
            "id": 1,
            "lineNumber": 1,
            "refNumber": "https://example.com",
            "transactionType": "https://example.com"
          },
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
      "pickBy": "2026-05-07T12:00:00.000Z",
      "priority": {
        "id": 1,
        "name": "Ava Chen"
      },
      "starred": 1,
      "summaryOnly": true,
      "syncToken": 1,
      "total": 1,
      "trackingNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `assignedToUser.id` | number |  |
| `assignedToUser.name` | string |  |
| `closed` | boolean |  |
| `comment` | string |  |
| `customer.fullname` | string |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `date` | date |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `lines` | array<object> |  |
| `lines[].altAmount` | number |  |
| `lines[].amount` | number |  |
| `lines[].backOrdered` | number |  |
| `lines[].description` | string |  |
| `lines[].duedate` | string |  |
| `lines[].id` | number |  |
| `lines[].invoiced` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].lineNumber` | number |  |
| `lines[].linkedTransaction.id` | number |  |
| `lines[].linkedTransaction.lineNumber` | number |  |
| `lines[].linkedTransaction.refNumber` | string |  |
| `lines[].linkedTransaction.transactionType` | string |  |
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
| `pickBy` | date |  |
| `priority.id` | number |  |
| `priority.name` | string |  |
| `starred` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |
| `total` | number |  |
| `trackingNumber` | string |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/pickticket` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pick-tickets.md) for the provider-specific parameters and requirements.

