# Zubie: Get Vehicle

Retrieves a vehicle from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-vehicle?connectionId=$CONNECTION_ID&vehicle_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vehicle_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/get-vehicle?${params}`, {
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
| `vehicle_key` | string | yes | Unique vehicle key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "nickname": "Ava Chen",
      "odometer": 1,
      "plate_number": "string",
      "vehicle_location": {},
      "vin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `nickname` | string |  |
| `odometer` | number |  |
| `plate_number` | string |  |
| `vehicle_location` | object |  |
| `vin` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /vehicle/{vehicle_key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vehicle.md) for the provider-specific parameters and requirements.

