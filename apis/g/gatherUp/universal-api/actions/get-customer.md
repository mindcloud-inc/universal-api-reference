# GatherUp: Get Customer

Retrieves detailed customer information from GatherUp.

```
GET https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/get-customer?${params}`, {
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
| `customerId` | number | yes | Customer id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": 1,
      "createdAt": "string",
      "customId": "string",
      "email": "ava@example.com",
      "errorCode": 1,
      "errorMessage": "string",
      "firstName": "Ava",
      "jobId": "string",
      "lastName": "Chen",
      "phone": "string",
      "rating": "string",
      "statusInfo": "string",
      "unsubscribed": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | number |  |
| `createdAt` | string |  |
| `customId` | string |  |
| `email` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `firstName` | string |  |
| `jobId` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `rating` | string |  |
| `statusInfo` | string |  |
| `unsubscribed` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /customer/get` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

