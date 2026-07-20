# Vtiger CRM: Create Product

Creates a new product in Vtiger CRM.

```
POST https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "element": {
    "productname": "Stage3 Default Product"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "element": {"productname":"Stage3 Default Product"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `element` | string | yes | JSON object string for the Product fields to create. Default: `{"productname":"Stage3 Default Product"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vtiger Product id. |
| `label` | string | Product label. |
| `url` | string | Product URL in Vtiger. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `POST /create?elementType=Products` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

