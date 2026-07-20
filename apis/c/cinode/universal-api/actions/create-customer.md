# Cinode: Create Customer

Creates a new customer in Cinode.

```
POST https://connect.mindcloud.co/v1/universal/cinode/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cinode/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Cinode company ID. |
| `name` | string | yes | Customer name. |
| `description` | string | no | Customer description. |
| `corporateIdentityNumber` | string | no | Customer corporate identity number. |
| `intermediator` | boolean | no | Whether the customer is an intermediary. |
| `size` | number | no | Company size enum. 0=Self employed, 1=2-10, 2=11-50, 3=51-200, 4=201-500, 5=501-1,000, 6=1,001-5,000, 7=5,001-10,000, 8=10,001+. |
| `turnOver` | number | no | Customer turnover. |
| `turnOverCurrencyId` | number | no | Currency ID for turnover. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "corporateIdentityNumber": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "email": "ava@example.com",
      "id": 1,
      "intermediator": true,
      "lastTouchDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "seoId": "string",
      "turnOver": 1,
      "updatedDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `corporateIdentityNumber` | string |  |
| `createdDateTime` | date |  |
| `description` | string |  |
| `email` | string |  |
| `id` | number |  |
| `intermediator` | boolean |  |
| `lastTouchDateTime` | date |  |
| `name` | string |  |
| `seoId` | string |  |
| `turnOver` | number |  |
| `updatedDateTime` | date |  |

## Native endpoint

Through the native Cinode API, this operation is `POST /v0.1/companies/:companyId/customers` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

