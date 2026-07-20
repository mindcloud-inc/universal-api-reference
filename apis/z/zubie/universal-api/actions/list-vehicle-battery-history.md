# Zubie: List Vehicle Battery History

Retrieves vehicle battery history from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-vehicle-battery-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-vehicle-battery-history?connectionId=$CONNECTION_ID&vehicle_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vehicle_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-vehicle-battery-history?${params}`, {
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
      "battery_level": 1,
      "battery_volts": 1,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `battery_level` | number |  |
| `battery_volts` | number |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /vehicle/{vehicle_key}/battery-history` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicle-battery-history.md) for the provider-specific parameters and requirements.

