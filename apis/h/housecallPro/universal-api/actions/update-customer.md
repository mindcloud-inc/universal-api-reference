# Housecall Pro: Update Customer



```
PUT https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "cus_a6d9f6f396e240749a6d216f10e382ae"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "cus_a6d9f6f396e240749a6d216f10e382ae"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | ID of the customer to update. Example: `cus_a6d9f6f396e240749a6d216f10e382ae`. |
| `firstName` | string | no | Example: `Stage`. |
| `lastName` | string | no | Example: `Three Updated`. |
| `email` | string | no | Example: `apps+stage3-update@mindcloud.co`. |
| `company` | string | no | Example: `MindCloud`. |
| `notificationsEnabled` | boolean | no |  |
| `mobileNumber` | string | no | Example: `2132135312`. |
| `homeNumber` | string | no | Example: `2132135313`. |
| `workNumber` | string | no | Example: `2132135314`. |
| `tags[]` | array<string> | no | Accepts multiple values as an array. Example: `vip`. |
| `leadSource` | string | no | Example: `web`. |
| `notes` | string | no | Example: `Updated during stage 3 buildout.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "company": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "homeNumber": "string",
      "id": "string",
      "lastName": "Chen",
      "leadSource": "string",
      "mobileNumber": "string",
      "notes": "string",
      "notificationsEnabled": true,
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "workNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `company` | string |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `homeNumber` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `leadSource` | string |  |
| `mobileNumber` | string |  |
| `notes` | string |  |
| `notificationsEnabled` | boolean |  |
| `tags` | array<string> |  |
| `updatedAt` | string |  |
| `workNumber` | string |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `PUT /customers/:customer_id` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

