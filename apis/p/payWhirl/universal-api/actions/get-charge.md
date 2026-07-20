# PayWhirl: Get Charge

Retrieves a charge from PayWhirl by ID.

```
GET https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-charge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-charge?connectionId=$CONNECTION_ID&chargeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chargeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/get-charge?${params}`, {
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
| `chargeId` | number | yes | The PayWhirl charge ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "billFee": 1,
      "createdAt": "string",
      "currency": "string",
      "customerId": 1,
      "deletedAt": "string",
      "description": "string",
      "fee": 1,
      "gatewayId": 1,
      "gatewayReference": "string",
      "id": 1,
      "refunded": 1,
      "refundedAmount": 1,
      "refundedOn": 1,
      "refundReference": "string",
      "updatedAt": "string",
      "usd": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `billFee` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customerId` | number |  |
| `deletedAt` | string |  |
| `description` | string |  |
| `fee` | number |  |
| `gatewayId` | number |  |
| `gatewayReference` | string |  |
| `id` | number |  |
| `refunded` | number |  |
| `refundedAmount` | number |  |
| `refundedOn` | number |  |
| `refundReference` | string |  |
| `updatedAt` | string |  |
| `usd` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `GET /charge/{id}` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charge.md) for the provider-specific parameters and requirements.

