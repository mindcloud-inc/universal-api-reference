# PayWhirl: List Customer Addresses

Retrieves a customer's addresses from PayWhirl.

```
GET https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customer-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customer-addresses?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customer-addresses?${params}`, {
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
| `customerId` | number | yes | The PayWhirl customer ID. |

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
      "customerId": 1,
      "deletedAt": "string",
      "firstName": "Ava",
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
| `customerId` | number |  |
| `deletedAt` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `metadata` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `updatedAt` | string |  |
| `userId` | number |  |
| `zip` | string |  |

## Native endpoint

Through the native PayWhirl API, this operation is `GET /customer/addresses/{id}` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-addresses.md) for the provider-specific parameters and requirements.

