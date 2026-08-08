# Fraser Direct: Get inventory



```
GET https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fraser Direct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory?connectionId=$CONNECTION_ID&groupByLot=N&includeInPick=N" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupByLot": "N",
  "includeInPick": "N"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory?${params}`, {
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
| `groupByLot` | list | yes | Required. Use Y to group inventory by lot or N to aggregate across lots. One of: `0`, `1`. Default: `N`. |
| `includeInPick` | list | yes | Required. Use Y to include inventory currently in picking or N to exclude it. One of: `0`, `1`. Default: `N`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupByLot": "string",
      "includeInPick": "string",
      "inventoryItems": [
        {}
      ],
      "recordCount": 1,
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupByLot` | string |  |
| `includeInPick` | string |  |
| `inventoryItems` | array<object> |  |
| `recordCount` | number |  |
| `success` | string |  |

## Native endpoint

Through the native Fraser Direct API, this operation is `GET /GetInventory` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory.md) for the provider-specific parameters and requirements.

