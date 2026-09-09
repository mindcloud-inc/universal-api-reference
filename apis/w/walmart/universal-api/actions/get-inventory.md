# Walmart: Get Inventory

Retrieve the current inventory for a single SKU.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inventory?connectionId=$CONNECTION_ID&sku=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sku": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inventory?${params}`, {
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
| `shipNode` | list<list> | no | The unique ID of the ship node (fulfillment center) whose inventory you want to retrieve. If you omit this parameter, the response includes inventory for every ship node linked to your seller account. Example: `e.g. 100009`. |
| `sku` | string | yes | A unique alphanumeric ID you assign to each item. Use the same value in every request that references the item, including your XSD catalog file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isDynamicSandbox` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "quantity": {
        "amount": 1,
        "unit": "string"
      },
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `quantity.amount` | number |  |
| `quantity.unit` | string |  |
| `sku` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/inventory` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory.md) for the provider-specific parameters and requirements.

