# Aspire: Create Item Allocation

Creates a new pay code in your Aspire account.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-item-allocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-item-allocation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "AllocationDate": "string",
  "CatalogItemID": 1,
  "InventoryLocationID": 1,
  "WorkTicketID": 1,
  "Quantity": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-item-allocation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "AllocationDate": "string",
    "CatalogItemID": 1,
    "InventoryLocationID": 1,
    "WorkTicketID": 1,
    "Quantity": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `AllocationDate` | string | yes |  |
| `CatalogItemID` | list<number> | yes |  |
| `InventoryLocationID` | list<number> | yes |  |
| `WorkTicketID` | list<number> | yes |  |
| `Quantity` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | boolean |  |

## Native endpoint

Through the native Aspire API, this operation is `POST ItemAllocations` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item-allocation.md) for the provider-specific parameters and requirements.

