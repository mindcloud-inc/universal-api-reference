# Bridge: Get Payment Link

Retrieves a payment link from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payment-link?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-payment-link?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiredAt": "2026-05-07T12:00:00.000Z",
      "fundInformation": {},
      "id": "string",
      "link": "https://example.com",
      "paymentStatus": "string",
      "status": "string",
      "transactions": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "companyName": "Ava Chen",
        "email": "ava@example.com",
        "externalReference": "string",
        "firstName": "Ava",
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
| `clientReference` | string | A reference to link this link to your system (100 char. max) |
| `createdAt` | date |  |
| `expiredAt` | date |  |
| `fundInformation` | object |  |
| `id` | string |  |
| `link` | string | Payment link's URL |
| `paymentStatus` | string |  |
| `status` | string |  |
| `transactions` | array<object> |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `user.companyName` | string | The company name |
| `user.email` | string | The user email |
| `user.externalReference` | string | We recommend filling this value with a unique ID that identifies your user.  It helps Bridge optimize fraud detection by tracking how many payments have been initiated by a single user within a specific period. |
| `user.firstName` | string | The user first name |
| `user.lastName` | string | The user last name |

## Native endpoint

Through the native Bridge API, this operation is `GET /payment/payment-links/:id` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-link.md) for the provider-specific parameters and requirements.

