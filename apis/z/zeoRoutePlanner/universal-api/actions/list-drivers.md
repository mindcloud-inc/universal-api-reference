# Zeo Route Planner: List Drivers

Retrieves drivers from Zeo Route Planner.

```
GET https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-drivers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-drivers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/list-drivers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "countryCodeName": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "phoneNo": "string",
      "postalCode": "string",
      "vehicleType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Driver address when available. |
| `countryCodeName` | string | Driver phone country code name when available. |
| `email` | string | Driver email address. |
| `id` | number | Driver identifier. |
| `latitude` | number | Driver latitude when available. |
| `longitude` | number | Driver longitude when available. |
| `name` | string | Driver name. |
| `phoneNo` | string | Driver phone number. |
| `postalCode` | string | Postal code when available. |
| `vehicleType` | string | Assigned vehicle type. |

## Native endpoint

Through the native Zeo Route Planner API, this operation is `GET /api/v5/drivers` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-drivers.md) for the provider-specific parameters and requirements.

