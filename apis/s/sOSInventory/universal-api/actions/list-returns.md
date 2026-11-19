# SOS Inventory: List Returns



```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-returns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-returns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-returns?${params}`, {
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
| `query` | string | no | Match return number, comment, or customer name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | list<string> | no | One of: `no`, `yes`. |
| `from` | date | no | Example: `2026-01-01T00:00:00`. |
| `to` | date | no | Example: `2026-01-01T00:00:00`. |
| `location` | list<string> | no |  |
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
      "channel": {
        "id": 1,
        "name": "Ava Chen"
      },
      "comment": "string",
      "createBillForShippingAmount": true,
      "createCreditMemo": true,
      "currency": {
        "id": 1,
        "name": "Ava Chen"
      },
      "customer": {
        "fullname": "Ava Chen",
        "id": 1,
        "name": "Ava Chen"
      },
      "customerMessage": "string",
      "customerNotes": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "exchangeRate": 1,
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
          "duedate": "string",
          "id": 1,
          "invoiced": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "lineNumber": 1,
          "lot": {
            "id": 1,
            "name": "Ava Chen"
          },
          "picked": 1,
          "produced": 1,
          "quantity": 1,
          "returned": 1,
          "shipped": 1,
          "unitprice": 1,
          "uom": {
            "id": 1,
            "name": "Ava Chen"
          },
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
      "shipBy": "string",
      "shippingAmount": 1,
      "shippingMethod": {
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
| `channel.id` | number |  |
| `channel.name` | string |  |
| `comment` | string |  |
| `createBillForShippingAmount` | boolean |  |
| `createCreditMemo` | boolean |  |
| `currency.id` | number |  |
| `currency.name` | string |  |
| `customer.fullname` | string |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customerMessage` | string |  |
| `customerNotes` | string |  |
| `date` | date |  |
| `exchangeRate` | number |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `lines` | array<object> |  |
| `lines[].altAmount` | number |  |
| `lines[].amount` | number |  |
| `lines[].backOrdered` | number |  |
| `lines[].class.id` | number |  |
| `lines[].class.name` | string |  |
| `lines[].description` | string |  |
| `lines[].duedate` | string |  |
| `lines[].id` | number |  |
| `lines[].invoiced` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].lineNumber` | number |  |
| `lines[].lot.id` | number |  |
| `lines[].lot.name` | string |  |
| `lines[].picked` | number |  |
| `lines[].produced` | number |  |
| `lines[].quantity` | number |  |
| `lines[].returned` | number |  |
| `lines[].shipped` | number |  |
| `lines[].unitprice` | number |  |
| `lines[].uom.id` | number |  |
| `lines[].uom.name` | string |  |
| `lines[].volume` | number |  |
| `lines[].volumeunit` | string |  |
| `lines[].weight` | number |  |
| `lines[].weightunit` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `number` | string |  |
| `shipBy` | string |  |
| `shippingAmount` | number |  |
| `shippingMethod.id` | number |  |
| `shippingMethod.name` | string |  |
| `starred` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |
| `total` | number |  |
| `trackingNumber` | string |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/return` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-returns.md) for the provider-specific parameters and requirements.

