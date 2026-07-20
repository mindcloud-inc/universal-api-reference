# GoAffPro: List Payment Requests

Retrieves affiliate payment requests from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-payment-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-payment-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-payment-requests?${params}`, {
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
| `affiliateId` | string | no | Only return payment requests for this affiliate ID. |
| `status` | string | no | Only return payment requests with this status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliate": {
        "affiliateId": 1,
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "affiliateId": 1,
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "invoiceUrl": "https://example.com",
      "note": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliate.affiliateId` | number | Nested affiliate ID. |
| `affiliate.email` | string | Affiliate email. |
| `affiliate.name` | string | Affiliate name. |
| `affiliateId` | number | Affiliate ID for the payment request. |
| `amount` | number | Payment request amount. |
| `createdAt` | date | Payment request creation timestamp. |
| `id` | number | Payment request ID. |
| `invoiceUrl` | string | Payment request invoice URL. |
| `note` | string | Payment request note. |
| `status` | string | Payment request status. |
| `updatedAt` | date | Payment request update timestamp. |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/payments/requests` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-requests.md) for the provider-specific parameters and requirements.

