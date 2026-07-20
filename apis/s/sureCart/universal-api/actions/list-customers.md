# SureCart: List Customers



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Only return customers with the given email address. Example: `customer@example.com`. |
| `liveMode` | boolean | no | Only return customers that are live mode or test mode. |
| `query` | string | no | Full-text search query for the customer collection. Example: `codex`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliationExpiresAt": 1,
      "billingAddress": "string",
      "billingMatchesShipping": true,
      "createdAt": 1,
      "defaultPaymentMethod": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "indexed": true,
      "lastName": "Chen",
      "liveMode": true,
      "name": "Ava Chen",
      "object": "string",
      "phone": "string",
      "portalUrl": "https://example.com",
      "shippingAddress": "string",
      "taxEnabled": true,
      "taxIdentifier": "string",
      "unsubscribed": true,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliationExpiresAt` | number |  |
| `billingAddress` | string |  |
| `billingMatchesShipping` | boolean |  |
| `createdAt` | number |  |
| `defaultPaymentMethod` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `indexed` | boolean |  |
| `lastName` | string |  |
| `liveMode` | boolean |  |
| `name` | string |  |
| `object` | string |  |
| `phone` | string |  |
| `portalUrl` | string |  |
| `shippingAddress` | string |  |
| `taxEnabled` | boolean |  |
| `taxIdentifier` | string |  |
| `unsubscribed` | boolean |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native SureCart API, this operation is `GET v1/customers` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

