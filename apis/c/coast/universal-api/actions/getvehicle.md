# Coast: Get Vehicle By ID



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getvehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getvehicle?connectionId=$CONNECTION_ID&vehicleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vehicleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getvehicle?${params}`, {
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
| `vehicleId` | string | yes | Coast vehicle ID of the vehicle to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "active": true,
      "assignedPeopleIds": [
        "string"
      ],
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
| `assignedPeopleIds[]` | string |  |
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

Through the native Coast API, this operation is `GET /v2/vehicles/:vehicleId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getvehicle.md) for the provider-specific parameters and requirements.

