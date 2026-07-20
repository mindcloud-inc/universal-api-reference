# Goldbelly: Bulk Update Subproducts



```
PUT https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-subproducts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goldbelly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-subproducts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subproducts[]": [
    {}
  ],
  "subproducts[].sku": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-subproducts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subproducts[]": [{}],
    "subproducts[].sku": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subproducts[]` | array<object> | yes | Subproducts to update. Each item must include SKU and may include inventory. |
| `subproducts[].sku` | string | yes | Subproduct SKU. |
| `subproducts[].inventory` | number | no | Subproduct inventory quantity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {
          "sku": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors[].sku` | string | 422 response error keyed by SKU when subproduct update fails. |

## Native endpoint

Through the native Goldbelly API, this operation is `POST subproducts/bulk_update` (base URL `https://api.goldbelly.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-subproducts.md) for the provider-specific parameters and requirements.

