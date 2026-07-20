# Leap: Update Customer

Updates an existing customer in Leap.

```
PUT https://connect.mindcloud.co/v1/universal/leap/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leap/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "first_name": "Ava",
  "last_name": "Chen",
  "phone_0_label": "string",
  "phone_0_number": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leap/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "first_name": "Ava",
    "last_name": "Chen",
    "phone_0_label": "string",
    "phone_0_number": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Leap customer ID. |
| `email` | string | no | Email address for the customer. |
| `first_name` | string | yes | First name of the customer. |
| `last_name` | string | yes | Last name of the customer. |
| `note` | string | no | Internal note to store on the customer. |
| `phone_0_label` | string | yes | Label for the primary phone number, for example cell or home. |
| `phone_0_number` | number | yes | Primary phone number for the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object | Updated customer returned by Leap. |
| `message` | string | Provider success message. |
| `status` | number | HTTP-style status code returned by Leap. |

## Native endpoint

Through the native Leap API, this operation is `PUT /customers/[:customerId]` (base URL `https://api.jobprogress.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

