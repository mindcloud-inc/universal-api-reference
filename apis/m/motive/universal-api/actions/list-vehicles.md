# Motive: List vehicles



```
GET https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Motive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-vehicles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-vehicles?${params}`, {
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
| `updatedAfter` | date | no | Return vehicles updated after the given UTC timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "vehicle": {
        "availabilityDetails": {
          "availabilityStatus": "string",
          "updatedAt": "string",
          "updatedByUser": {}
        },
        "carbCtcEmissionStatus": {},
        "carbCtcTestEnabled": {},
        "companyId": 1,
        "createdAt": "string",
        "currentDriver": {},
        "driverFacingCamera": 1,
        "eldDevice": {
          "id": 1,
          "identifier": "string",
          "model": "string"
        },
        "fuelType": "string",
        "groupIds": [
          1
        ],
        "id": 1,
        "ifta": true,
        "incabAlertLiveStreamEnable": 1,
        "incabAudioRecording": 1,
        "licensePlateCountryCode": {},
        "licensePlateNumber": "string",
        "licensePlateState": "string",
        "make": "string",
        "metricUnits": true,
        "model": "string",
        "notes": "string",
        "number": "string",
        "permanentDriver": {},
        "preventAutoOdometerEntry": true,
        "registrationExpiryDate": {},
        "status": "string",
        "updatedAt": "string",
        "vin": "string",
        "year": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `vehicle.availabilityDetails.availabilityStatus` | string |  |
| `vehicle.availabilityDetails.updatedAt` | string |  |
| `vehicle.availabilityDetails.updatedByUser` | object |  |
| `vehicle.carbCtcEmissionStatus` | object |  |
| `vehicle.carbCtcTestEnabled` | object |  |
| `vehicle.companyId` | number |  |
| `vehicle.createdAt` | string |  |
| `vehicle.currentDriver` | object |  |
| `vehicle.driverFacingCamera` | number |  |
| `vehicle.eldDevice.id` | number |  |
| `vehicle.eldDevice.identifier` | string |  |
| `vehicle.eldDevice.model` | string |  |
| `vehicle.fuelType` | string |  |
| `vehicle.groupIds[]` | number |  |
| `vehicle.id` | number |  |
| `vehicle.ifta` | boolean |  |
| `vehicle.incabAlertLiveStreamEnable` | number |  |
| `vehicle.incabAudioRecording` | number |  |
| `vehicle.licensePlateCountryCode` | object |  |
| `vehicle.licensePlateNumber` | string |  |
| `vehicle.licensePlateState` | string |  |
| `vehicle.make` | string |  |
| `vehicle.metricUnits` | boolean |  |
| `vehicle.model` | string |  |
| `vehicle.notes` | string |  |
| `vehicle.number` | string |  |
| `vehicle.permanentDriver` | object |  |
| `vehicle.preventAutoOdometerEntry` | boolean |  |
| `vehicle.registrationExpiryDate` | object |  |
| `vehicle.status` | string |  |
| `vehicle.updatedAt` | string |  |
| `vehicle.vin` | string |  |
| `vehicle.year` | string |  |

## Native endpoint

Through the native Motive API, this operation is `GET /v1/vehicles` (base URL `https://api.gomotive.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vehicles.md) for the provider-specific parameters and requirements.

