# Coast: Get All Purchases



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpurchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpurchases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getpurchases?${params}`, {
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
| `nextPageToken` | string | no | A token that represents the next page of results. Use the token returned by a previous response to retrieve the next page of purchases. |
| `pageSize` | number | no | The maximum number of purchases to return per page. |
| `status` | list | no | Only return purchases with this status. One of: `0`, `1`, `2`. |
| `completedStartingAt` | string | no | Only return purchases completed on or after this date. |
| `completedEndingBefore` | string | no | Only return purchases completed before this date. |
| `createdStartingAt` | string | no | Only return purchases created on or after this date. |
| `createdEndingBefore` | string | no | Only return purchases created before this date. |
| `assignedPersonId` | string | no | Only return purchases assigned to this Coast person ID. |
| `assignedPersonDepartmentId` | string | no | Only return purchases whose assigned person belongs to this Coast department ID. |
| `assignedPersonLocationId` | string | no | Only return purchases whose assigned person belongs to this Coast location ID. |
| `assignedPersonPolicyId` | string | no | Only return purchases whose assigned person uses this Coast policy ID. |
| `assignedVehicleId` | string | no | Only return purchases assigned to this Coast vehicle ID. |
| `assignedVehicleDepartmentId` | string | no | Only return purchases whose assigned vehicle belongs to this Coast department ID. |
| `assignedVehicleLocationId` | string | no | Only return purchases whose assigned vehicle belongs to this Coast location ID. |
| `assignedVehiclePolicyId` | string | no | Only return purchases whose assigned vehicle uses this Coast policy ID. |
| `cardId` | string | no | Only return purchases made with this Coast card ID. |
| `merchantLocationId` | string | no | Only return purchases from this Coast merchant location ID. |
| `merchantBrandId` | string | no | Only return purchases from this Coast merchant brand ID. |

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

Through the native Coast API, this operation is `GET /v2/transactions/purchases` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/getpurchases.md) for the provider-specific parameters and requirements.

