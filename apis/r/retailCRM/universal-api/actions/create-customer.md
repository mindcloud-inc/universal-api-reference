# retailCRM: Create Customer

Creates a new customer in retailCRM.

```
POST https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site": "string",
  "customer.externalId": "string",
  "customer.firstName": "Ava",
  "customer.phones[0].number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site": "string",
    "customer.externalId": "string",
    "customer.firstName": "Ava",
    "customer.phones[0].number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `site` | list | yes |  |
| `customer.externalId` | string | yes |  |
| `customer.firstName` | string | yes |  |
| `customer.lastName` | string | no |  |
| `customer.email` | string | no |  |
| `customer.phones[0].number` | string | yes |  |
| `customer.managerId` | list | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native retailCRM API, this operation is `POST /customers/create` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

