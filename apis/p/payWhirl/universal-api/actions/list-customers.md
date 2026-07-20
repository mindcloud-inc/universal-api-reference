# PayWhirl: List Customers

Retrieves customers from PayWhirl.

```
GET https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customers?${params}`, {
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
| `afterId` | number | no | Return customers with IDs greater than this value. |
| `beforeId` | number | no | Return customers with IDs lower than this value. |
| `keyword` | string | no | Optional keyword filter. |
| `limit` | number | no | Number of customer records to return. |
| `orderDirection` | string | no | Sort direction. Use asc or desc. |
| `orderKey` | string | no | Customer field to sort by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultCard": 1,
      "deletedAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "gatewayId": 1,
      "gatewayReference": "string",
      "gatewayType": "string",
      "id": 1,
      "lastName": "Chen",
      "metadata": "string",
      "phone": "string",
      "state": "string",
      "updatedAt": "string",
      "userId": 1,
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `defaultCard` | number |  |
| `deletedAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `gatewayId` | number |  |
| `gatewayReference` | string |  |
| `gatewayType` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `metadata` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |
| `zip` | string |  |

## Native endpoint

Through the native PayWhirl API, this operation is `GET /customers` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

