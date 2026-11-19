# SOS Inventory: List Adjustments



```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-adjustments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-adjustments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-adjustments?${params}`, {
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
| `query` | string | no | Match adjustment number, ID, comment, or location. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | list<string> | no | One of: `closed`, `open`. |
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
      "account": {
        "id": 1,
        "name": "Ava Chen"
      },
      "archived": true,
      "comment": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "forceSave": true,
      "hasSignature": true,
      "id": 1,
      "lines": [
        {
          "class": {
            "id": 1,
            "name": "Ava Chen"
          },
          "description": "string",
          "id": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "linenumber": 1,
          "lot": {
            "id": 1,
            "name": "Ava Chen"
          },
          "newQuantity": 1,
          "quantityDiff": 1,
          "uom": {
            "id": 1,
            "name": "Ava Chen"
          },
          "valueDiff": 1
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
| `account.id` | number |  |
| `account.name` | string |  |
| `archived` | boolean |  |
| `comment` | string |  |
| `date` | date |  |
| `forceSave` | boolean |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `lines` | array<object> |  |
| `lines[].class.id` | number |  |
| `lines[].class.name` | string |  |
| `lines[].description` | string |  |
| `lines[].id` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].linenumber` | number |  |
| `lines[].lot.id` | number |  |
| `lines[].lot.name` | string |  |
| `lines[].newQuantity` | number |  |
| `lines[].quantityDiff` | number |  |
| `lines[].uom.id` | number |  |
| `lines[].uom.name` | string |  |
| `lines[].valueDiff` | number |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `number` | string |  |
| `starred` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |
| `total` | number |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/adjustment` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-adjustments.md) for the provider-specific parameters and requirements.

