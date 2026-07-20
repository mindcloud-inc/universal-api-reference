# GoAffPro: List Payments

Retrieves payment history entries from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0&fields%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fields[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-payments?${params}`, {
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
| `affiliateId` | string | no | Only return payments for this affiliate ID. |
| `fields[]` | array<string> | yes | Fields to include in returned payments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adminNote": "string",
      "affiliateId": 1,
      "affiliateMessage": "string",
      "amount": 1,
      "createdAt": "string",
      "currency": "string",
      "id": 1,
      "paymentMethod": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adminNote` | string |  |
| `affiliateId` | number |  |
| `affiliateMessage` | string |  |
| `amount` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `id` | number |  |
| `paymentMethod` | string |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/payments` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

