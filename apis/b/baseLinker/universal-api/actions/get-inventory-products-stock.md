# BaseLinker: Get Inventory Products Stock

Retrieves inventory product stock from BaseLinker.

```
GET https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-inventory-products-stock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-inventory-products-stock?connectionId=$CONNECTION_ID&inventory_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inventory_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-inventory-products-stock?${params}`, {
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
| `inventory_id` | number | yes | Inventory identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters` | object | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BaseLinker API returns.

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-products-stock.md) for the provider-specific parameters and requirements.

