# GoCanvas: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Identifier of the customer to update. |
| `customerType` | list | no | Customer type. The documentation conflicts on whether it is required for PATCH. One of: `business`, `individual`. |
| `businessName` | string | no | Business name; documented as required for business customers. |
| `contactRole` | string | no | Role of the customer's contact person. |
| `contactFirstName` | string | no | Contact first name; documented as required for individual customers. |
| `contactLastName` | string | no | Contact last name; documented as required for individual customers. |
| `contactEmail` | string | no | Email of the contact person. |
| `contactPhone` | string | no | Phone of the contact person. |
| `contactPreference` | string | no | Preferred contact method. |
| `notes` | string | no | Longer description of the customer. |
| `defaultSiteId` | number | no | Primary site ID when multiple site IDs are provided. |
| `code` | string | no | Alphanumeric customer identifier. |
| `siteIds[]` | array<number> | no | Site IDs to add. The first is primary unless Default Site ID is provided. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `PATCH /customers/:customerId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

