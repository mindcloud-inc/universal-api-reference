# DataCrush: Update Ecommerce Customer

Updates an ecommerce customer in DataCrush.

```
PUT https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/update-ecommerce-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/update-ecommerce-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customers_json": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/update-ecommerce-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customers_json": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customers_json` | string | yes | JSON array of customer objects. Each object must include id, email, first_name, and last_name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /ecommerce/v1/customer/add` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ecommerce-customer.md) for the provider-specific parameters and requirements.

