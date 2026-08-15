# Samsara: List Vehicles



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-all-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-all-vehicles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-all-vehicles?${params}`, {
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
| `createdAfterTime` | string | no | Return vehicles created at or after this RFC 3339 timestamp. |
| `updatedAfterTime` | string | no | Return vehicles updated at or after this RFC 3339 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        {
          "id": "string",
          "name": "Ava Chen",
          "stringValues": [
            "string"
          ]
        }
      ],
      "cameraSerial": "string",
      "createdAtTime": "string",
      "externalIds": {
        "samsara": {
          "serial": "string",
          "vin": "string"
        }
      },
      "gateway": {
        "model": "string",
        "serial": "string"
      },
      "harshAccelerationSettingType": "string",
      "id": "string",
      "licensePlate": "string",
      "make": "string",
      "model": "string",
      "name": "Ava Chen",
      "notes": "string",
      "serial": "string",
      "staticAssignedDriver": {
        "id": "string",
        "name": "Ava Chen"
      },
      "tags": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "updatedAtTime": "string",
      "vehicleRegulationMode": "string",
      "vin": "string",
      "year": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes[].id` | string |  |
| `attributes[].name` | string |  |
| `attributes[].stringValues` | array<string> |  |
| `cameraSerial` | string |  |
| `createdAtTime` | string |  |
| `externalIds.samsara.serial` | string |  |
| `externalIds.samsara.vin` | string |  |
| `gateway.model` | string |  |
| `gateway.serial` | string |  |
| `harshAccelerationSettingType` | string |  |
| `id` | string |  |
| `licensePlate` | string |  |
| `make` | string |  |
| `model` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `serial` | string |  |
| `staticAssignedDriver.id` | string |  |
| `staticAssignedDriver.name` | string |  |
| `tags[].id` | string |  |
| `tags[].name` | string |  |
| `updatedAtTime` | string |  |
| `vehicleRegulationMode` | string |  |
| `vin` | string |  |
| `year` | string |  |

## Native endpoint

Through the native Samsara API, this operation is `GET fleet/vehicles` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-vehicles.md) for the provider-specific parameters and requirements.

