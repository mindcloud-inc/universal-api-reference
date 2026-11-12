# Jobber: Update Item



```
PUT https://connect.mindcloud.co/v1/universal/jobber/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jobber/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productOrServiceId": "Product or service ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jobber/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productOrServiceId": "Product or service ID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productOrServiceId` | string | yes | Jobber product or service ID to update. Example: `Product or service ID`. |
| `name` | string | no | Name of the product or service item. |
| `defaultUnitCost` | number | no | Default price for the service or product. |
| `category` | list | no | Whether this item is a product or a service. One of: `PRODUCT`, `SERVICE`. |
| `description` | string | no | Description for the service or product. |
| `taxable` | boolean | no | Whether the product or service is taxable. |
| `internalUnitCost` | number | no | Default internal unit cost for the product or service. |
| `markup` | number | no | Default markup for the product or service. |
| `durationMinutes` | number | no | Duration to complete the service in minutes. |
| `onlineBookingsEnabled` | boolean | no | Whether the product or service is available as a bookable service. |
| `visible` | boolean | no | Whether the product or service is visible for line-item autocomplete. |
| `bookableType` | list | no | Type of online booking created for this product or service. One of: `WORK_ORDER`, `WORK_REQUEST`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productOrService": {
        "bookableType": "string",
        "category": "string",
        "defaultUnitCost": 1,
        "description": "string",
        "durationMinutes": 1,
        "id": "string",
        "internalUnitCost": 1,
        "markup": 1,
        "name": "Ava Chen",
        "onlineBookingsEnabled": true,
        "taxable": true,
        "visible": true
      },
      "userErrors": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `productOrService.bookableType` | string | Type of online booking created for the product or service. |
| `productOrService.category` | string | Updated item category. |
| `productOrService.defaultUnitCost` | number | Default price for the product or service. |
| `productOrService.description` | string | Updated product or service description. |
| `productOrService.durationMinutes` | number | Service duration in minutes. |
| `productOrService.id` | string | Updated product or service ID. |
| `productOrService.internalUnitCost` | number | Default internal unit cost. |
| `productOrService.markup` | number | Default markup. |
| `productOrService.name` | string | Updated product or service name. |
| `productOrService.onlineBookingsEnabled` | boolean | Whether online booking is enabled. |
| `productOrService.taxable` | boolean | Whether the item is taxable. |
| `productOrService.visible` | boolean | Whether the item is visible for line-item autocomplete. |
| `userErrors` | array<object> | Jobber mutation validation errors. |

## Native endpoint

Through the native Jobber API, this operation is `POST graphql` (base URL `https://api.getjobber.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

