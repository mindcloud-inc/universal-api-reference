# Merit: Create Customer



```
POST https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "notTDCustomer": true,
  "countryCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/merit/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "notTDCustomer": true,
    "countryCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Unique customer name. |
| `notTDCustomer` | boolean | yes | For Estonia, true for physical persons and foreign companies. |
| `countryCode` | string | yes | Two-letter country code required when adding a customer. |
| `email` | string | no | Customer email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": "string",
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | string | Created customer identifier. |
| `Name` | string | Created customer name. |

## Native endpoint

Through the native Merit API, this operation is `POST v2/sendcustomer` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

