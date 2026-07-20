# Coast: Get Purchase By ID



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpurchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpurchase?connectionId=$CONNECTION_ID&purchaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpurchase?${params}`, {
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
| `purchaseId` | string | yes | Coast purchase ID of the purchase to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "amount": 1,
      "card": {
        "coastId": "string",
        "id": "string",
        "last4": "string"
      },
      "createdTime": "string",
      "id": "string",
      "memo": {},
      "merchantSnapshot": {
        "address": "string",
        "brand": {
          "id": "string",
          "logoUrl": {},
          "name": "Ava Chen"
        },
        "category": "string",
        "categoryCode": "string",
        "city": "string",
        "country": "string",
        "id": "string",
        "latitude": 1,
        "logoUrl": {},
        "longitude": 1,
        "name": "Ava Chen",
        "state": "string",
        "zip": "string"
      },
      "personSnapshot": {
        "department": {},
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "location": {},
        "policyId": "string"
      },
      "status": "string",
      "updatedTime": "string",
      "vehicleSnapshot": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `amount` | number |  |
| `card.coastId` | string |  |
| `card.id` | string |  |
| `card.last4` | string |  |
| `createdTime` | string |  |
| `id` | string |  |
| `memo` | object |  |
| `merchantSnapshot.address` | string |  |
| `merchantSnapshot.brand.id` | string |  |
| `merchantSnapshot.brand.logoUrl` | object |  |
| `merchantSnapshot.brand.name` | string |  |
| `merchantSnapshot.category` | string |  |
| `merchantSnapshot.categoryCode` | string |  |
| `merchantSnapshot.city` | string |  |
| `merchantSnapshot.country` | string |  |
| `merchantSnapshot.id` | string |  |
| `merchantSnapshot.latitude` | number |  |
| `merchantSnapshot.logoUrl` | object |  |
| `merchantSnapshot.longitude` | number |  |
| `merchantSnapshot.name` | string |  |
| `merchantSnapshot.state` | string |  |
| `merchantSnapshot.zip` | string |  |
| `personSnapshot.department` | object |  |
| `personSnapshot.firstName` | string |  |
| `personSnapshot.id` | string |  |
| `personSnapshot.lastName` | string |  |
| `personSnapshot.location` | object |  |
| `personSnapshot.policyId` | string |  |
| `status` | string |  |
| `updatedTime` | string |  |
| `vehicleSnapshot` | object |  |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/transactions/purchases/:purchaseId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getpurchase.md) for the provider-specific parameters and requirements.

