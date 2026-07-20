# Cheddar: Add Item Quantity

Increments a customer item quantity in Cheddar.

```
PUT https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/add-item-quantity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cheddar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/add-item-quantity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerCode": "string",
  "itemCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/add-item-quantity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerCode": "string",
    "itemCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerCode` | string | yes | Customer code from Cheddar. |
| `itemCode` | string | yes | Tracked item code from Cheddar. |
| `quantity` | number | no | Positive amount to add to the current tracked item usage. Defaults to 1.0000 when omitted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `remoteAddress` | string | no | Client IPv4 address for fraud protection and rate limiting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "quantity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `quantity` | number |  |

## Native endpoint

Through the native Cheddar API, this operation is `POST /customers/add-item-quantity/productCode/{{credentials.productCode}}/code/:customerCode/itemCode/:itemCode` (base URL `https://getcheddar.com/xml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-item-quantity.md) for the provider-specific parameters and requirements.

