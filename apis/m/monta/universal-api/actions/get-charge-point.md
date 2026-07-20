# Monta: Get Charge Point

Retrieves a charge point from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-charge-point
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-charge-point?connectionId=$CONNECTION_ID&chargePointId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chargePointId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-charge-point?${params}`, {
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
| `chargePointId` | number | yes | ID of the Monta charge point to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brandName": "Ava Chen",
      "cablePluggedIn": true,
      "connectors": [
        {
          "identifier": "string",
          "name": "Ava Chen"
        }
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "firmwareVersion": "string",
      "id": 1,
      "lastMeterReadingKwh": 1,
      "location": {
        "address": {
          "address1": "string",
          "city": "string",
          "country": "string"
        },
        "coordinates": {
          "latitude": 1,
          "longitude": 1
        }
      },
      "maxKw": 1,
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "note": "string",
      "serialNumber": "string",
      "state": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandName` | string |  |
| `cablePluggedIn` | boolean |  |
| `connectors[].identifier` | string |  |
| `connectors[].name` | string |  |
| `createdAt` | date |  |
| `firmwareVersion` | string |  |
| `id` | number |  |
| `lastMeterReadingKwh` | number |  |
| `location.address.address1` | string |  |
| `location.address.city` | string |  |
| `location.address.country` | string |  |
| `location.coordinates.latitude` | number |  |
| `location.coordinates.longitude` | number |  |
| `maxKw` | number |  |
| `modelName` | string |  |
| `name` | string |  |
| `note` | string |  |
| `serialNumber` | string |  |
| `state` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native Monta API, this operation is `GET /charge-points/{chargePointId}` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charge-point.md) for the provider-specific parameters and requirements.

