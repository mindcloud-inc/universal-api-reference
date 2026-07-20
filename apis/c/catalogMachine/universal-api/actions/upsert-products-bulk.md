# Catalog Machine: Upsert Products (Bulk)

Creates or updates multiple products in Catalog Machine.

```
PUT https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/upsert-products-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Catalog Machine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/upsert-products-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "products": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/upsert-products-bulk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "products": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `products` | list<object> | yes | Bulk products payload. Example: [{"Code":"CM-TEST-001","Name":"Codex Test Product 1"}] |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | number |  |

## Native endpoint

Through the native Catalog Machine API, this operation is `POST /products` (base URL `https://www.catalogmachine.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-products-bulk.md) for the provider-specific parameters and requirements.

