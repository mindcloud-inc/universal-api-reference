# PayWhirl: List Plans

Retrieves subscription plans from PayWhirl.

```
GET https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-plans?${params}`, {
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
| `afterId` | number | no | Return plans with IDs greater than this value. |
| `beforeId` | number | no | Return plans with IDs lower than this value. |
| `limit` | number | no | Number of plan records to return. |
| `orderDirection` | string | no | Sort direction. Use asc or desc. |
| `orderKey` | string | no | Plan field to sort by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "billingAmount": 1,
      "billingFrequency": "string",
      "billingInterval": 1,
      "createdAt": "string",
      "currency": "string",
      "deletedAt": "string",
      "description": "string",
      "enabled": 1,
      "id": 1,
      "image": "string",
      "installments": 1,
      "metadata": "string",
      "name": "Ava Chen",
      "requireTax": 1,
      "setupFee": 1,
      "setupFeeType": "string",
      "sku": "string",
      "trialDays": 1,
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `billingAmount` | number |  |
| `billingFrequency` | string |  |
| `billingInterval` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `deletedAt` | string |  |
| `description` | string |  |
| `enabled` | number |  |
| `id` | number |  |
| `image` | string |  |
| `installments` | number |  |
| `metadata` | string |  |
| `name` | string |  |
| `requireTax` | number |  |
| `setupFee` | number |  |
| `setupFeeType` | string |  |
| `sku` | string |  |
| `trialDays` | number |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `GET /plans` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

