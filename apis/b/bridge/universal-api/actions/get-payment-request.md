# Bridge: Get Payment Request

Retrieves a payment request from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payment-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payment-request?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientReference": "string",
      "createdAt": "string",
      "id": "string",
      "paymentLinkId": "https://example.com",
      "providerId": 1,
      "sender": {
        "iban": "string",
        "name": "Ava Chen"
      },
      "status": "string",
      "statusReason": "string",
      "transactions": "string",
      "updatedAt": "string",
      "user": {
        "companyName": "Ava Chen",
        "email": "ava@example.com",
        "externalReference": "string",
        "firstName": "Ava",
        "ipAddress": "string",
        "lastName": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientReference` | string | A reference you can specify to optimize your payment request reconciliation.  This reference will also be available when you retrieve the payment status using Bridge endpoints.  There is a similar field in the transaction resource that can be used to reconcile individual transactions. |
| `createdAt` | string | The payment request creation date |
| `id` | string | Payment request's unique identifier |
| `paymentLinkId` | string | The payment link's unique identifier |
| `providerId` | number | The provider's unique identifier |
| `sender` | object |  |
| `sender.iban` | string | The sender iban information communicated by the provider |
| `sender.name` | string | The sender name information communicated by the provider |
| `status` | string | Payment request's status |
| `statusReason` | string | Payment request's status reason |
| `transactions` | string |  |
| `updatedAt` | string | The payment request last update date |
| `user` | object |  |
| `user.companyName` | string | The company name |
| `user.email` | string | The user email |
| `user.externalReference` | string | We recommend filling this value with a unique ID that identifies your user.  It helps Bridge optimize fraud detection by tracking how many payments have been initiated by a single user within a specific period. |
| `user.firstName` | string | The user first name |
| `user.ipAddress` | string | The user's IP address |
| `user.lastName` | string | The user last name |

## Native endpoint

Through the native Bridge API, this operation is `GET /payment/payment-requests/:id` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-request.md) for the provider-specific parameters and requirements.

