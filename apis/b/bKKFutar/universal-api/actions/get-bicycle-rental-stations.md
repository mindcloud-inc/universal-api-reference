# BKK Futar: Get Bicycle Rental Stations

Retrieves bicycle rental stations from BKK Futar.

```
GET https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-bicycle-rental-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BKK Futar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-bicycle-rental-stations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/get-bicycle-rental-stations?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_references` | string | no | Reference data to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limitExceeded": true,
      "list": {
        "bikes": 1,
        "code": "string",
        "id": "string",
        "lat": 1,
        "lon": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "references": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limitExceeded` | boolean | Whether the response exceeded the defined limit. |
| `list` | array<object> | Bicycle rental stations. |
| `list.bikes` | number | Number of available bikes. |
| `list.code` | string | Station code. |
| `list.id` | string | Bike station ID. |
| `list.lat` | number | Station latitude. |
| `list.lon` | number | Station longitude. |
| `list.name` | string | Station name. |
| `list.type` | string | Station type. |
| `references` | object | Included reference details. |

## Native endpoint

Through the native BKK Futar API, this operation is `GET /bicycle-rental.json` (base URL `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bicycle-rental-stations.md) for the provider-specific parameters and requirements.

