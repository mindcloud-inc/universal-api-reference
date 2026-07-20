# Aspire: List Work Ticket Items

Retrieves work ticket items from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-items?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocationUnitTypeID": 1,
      "allocationUnitTypeName": "Ava Chen",
      "autoExpense": true,
      "catalogItemCategoryID": 1,
      "catalogItemCategoryName": "Ava Chen",
      "catalogItemID": 1,
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "doNotPurchase": true,
      "estimatingNotes": {},
      "itemCost": 1,
      "itemName": "Ava Chen",
      "itemQuantityExtended": 1,
      "itemType": "string",
      "showOnTicket": true,
      "workTicketID": 1,
      "workTicketItemID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocationUnitTypeID` | number |  |
| `allocationUnitTypeName` | string |  |
| `autoExpense` | boolean |  |
| `catalogItemCategoryID` | number |  |
| `catalogItemCategoryName` | string |  |
| `catalogItemID` | number |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `doNotPurchase` | boolean |  |
| `estimatingNotes` | object |  |
| `itemCost` | number |  |
| `itemName` | string |  |
| `itemQuantityExtended` | number |  |
| `itemType` | string |  |
| `showOnTicket` | boolean |  |
| `workTicketID` | number |  |
| `workTicketItemID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET WorkTicketItems` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-ticket-items.md) for the provider-specific parameters and requirements.

