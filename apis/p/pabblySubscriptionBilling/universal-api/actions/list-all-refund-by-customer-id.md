# Pabbly Subscription Billing: List All Refund By Customer Id



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-refund-by-customer-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-refund-by-customer-id?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-refund-by-customer-id?${params}`, {
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
| `customerId` | string | no |  |
| `invoiceId` | string | no |  |
| `planId` | string | no |  |
| `productId` | string | no |  |
| `status` | string | no |  |
| `subscriptionId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "description": "string",
      "gatewayType": "string",
      "id": "string",
      "invoiceId": "string",
      "planId": "string",
      "productId": "string",
      "referenceId": "string",
      "referenceNumber": "string",
      "status": "string",
      "statusFormatted": "string",
      "subscriptionId": "string",
      "type": "string",
      "typeFormated": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdAt` | date |  |
| `customerId` | string |  |
| `description` | string |  |
| `gatewayType` | string |  |
| `id` | string |  |
| `invoiceId` | string |  |
| `planId` | string |  |
| `productId` | string |  |
| `referenceId` | string |  |
| `referenceNumber` | string |  |
| `status` | string |  |
| `statusFormatted` | string |  |
| `subscriptionId` | string |  |
| `type` | string |  |
| `typeFormated` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/refund/:customerId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-refund-by-customer-id.md) for the provider-specific parameters and requirements.

