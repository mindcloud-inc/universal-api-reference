# GoCanvas: Create Customer



```
POST https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerType": "business"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerType": "business"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerType` | list | yes | An individual or a business customer. One of: `business`, `individual`. |
| `businessName` | string | no | Required when customer type is business. |
| `contactRole` | string | no | Role of the customer's contact person. |
| `contactFirstName` | string | no | Required when customer type is individual. |
| `contactLastName` | string | no | Required when customer type is individual. |
| `contactEmail` | string | no | Email address of the customer's contact person. |
| `contactPhone` | string | no | Phone number of the customer's contact person. |
| `contactPreference` | string | no | Preferred method of contact. |
| `notes` | string | no | Longer description of the customer. |
| `code` | string | no | Alphanumeric code uniquely identifying the customer. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `POST /customers` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

