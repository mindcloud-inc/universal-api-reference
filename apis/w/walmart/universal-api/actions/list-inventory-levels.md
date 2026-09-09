# Walmart: List Inventory Levels

Retrieve the inventory level for every SKU at every ship node.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-inventory-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-inventory-levels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-inventory-levels?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sandboxToken` | list<string> | no | To run this request in the walmart sandbox choose 'bearer' token from the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inventoryAvailableDate": "string",
      "quantity": {
        "amount": 1,
        "unit": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inventoryAvailableDate` | string |  |
| `quantity.amount` | number |  |
| `quantity.unit` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/inventories` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-levels.md) for the provider-specific parameters and requirements.

