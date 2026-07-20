# retailCRM: Update Customer

Updates an existing customer in retailCRM.

```
PUT https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string",
  "site": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string",
    "site": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes |  |
| `by` | list | no | One of: `externalId`, `id`. Default: `externalId`. |
| `site` | list | yes |  |
| `customer.firstName` | string | no |  |
| `customer.lastName` | string | no |  |
| `customer.email` | string | no |  |
| `customer.phones[0].number` | string | no |  |
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

Through the native retailCRM API, this operation is `POST /customers/:externalId/edit` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

