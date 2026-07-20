# Coast: Get All Vehicles



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getvehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getvehicles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getvehicles?${params}`, {
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
| `nextPageToken` | string | no | A token that represents the next page of results. Use the token returned by a previous response to retrieve the next page of vehicles. |
| `pageSize` | number | no | The maximum number of vehicles to return per page. |
| `active` | boolean | no | Only return vehicles with this active status. |
| `departmentId` | string | no | Only return vehicles assigned to this Coast department ID. |
| `locationId` | string | no | Only return vehicles assigned to this Coast location ID. |
| `policyId` | string | no | Only return vehicles assigned to this Coast policy ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "active": true,
      "createdTime": "string",
      "departmentDetails": {},
      "departmentId": {},
      "fuelType": "string",
      "id": "string",
      "largeTankMaxAuthAmount": {},
      "licensePlate": "string",
      "licensePlateState": "string",
      "locationDetails": {},
      "locationId": {},
      "make": "string",
      "model": "string",
      "modelYear": 1,
      "name": "Ava Chen",
      "policyDetails": {},
      "policyId": {},
      "source": {
        "id": "string",
        "type": "string"
      },
      "tankCapacity": {},
      "updatedTime": "string",
      "vin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `active` | boolean |  |
| `createdTime` | string |  |
| `departmentDetails` | object |  |
| `departmentId` | object |  |
| `fuelType` | string |  |
| `id` | string |  |
| `largeTankMaxAuthAmount` | object |  |
| `licensePlate` | string |  |
| `licensePlateState` | string |  |
| `locationDetails` | object |  |
| `locationId` | object |  |
| `make` | string |  |
| `model` | string |  |
| `modelYear` | number |  |
| `name` | string |  |
| `policyDetails` | object |  |
| `policyId` | object |  |
| `source.id` | string |  |
| `source.type` | string |  |
| `tankCapacity` | object |  |
| `updatedTime` | string |  |
| `vin` | string |  |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/vehicles` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/getvehicles.md) for the provider-specific parameters and requirements.

