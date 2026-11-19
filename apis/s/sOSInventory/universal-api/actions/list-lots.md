# SOS Inventory: List Lots



```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-lots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-lots?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-lots?${params}`, {
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
| `query` | string | no | Match lot number, description, or item name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | list<string> | no | One of: `expired`, `notexpirednotrecalled`, `recalled`. |
| `archived` | list<string> | no | One of: `no`, `yes`. |
| `location` | list<string> | no | Calculate quantity totals for this location. |
| `createdSince` | date | no | Example: `2026-01-01T00:00:00`. |
| `updatedSince` | date | no | Example: `2026-01-01T00:00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "available": 1,
      "description": "string",
      "expiration": "2026-05-07T12:00:00.000Z",
      "expired": true,
      "id": 1,
      "item": {
        "id": 1,
        "name": "Ava Chen"
      },
      "itemDescription": "string",
      "number": "string",
      "onhand": 1,
      "recalled": true,
      "starred": 1,
      "summaryOnly": true,
      "syncToken": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `available` | number |  |
| `description` | string |  |
| `expiration` | date |  |
| `expired` | boolean |  |
| `id` | number |  |
| `item.id` | number |  |
| `item.name` | string |  |
| `itemDescription` | string |  |
| `number` | string |  |
| `onhand` | number |  |
| `recalled` | boolean |  |
| `starred` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/lot` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-lots.md) for the provider-specific parameters and requirements.

