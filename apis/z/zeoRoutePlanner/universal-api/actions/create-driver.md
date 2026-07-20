# Zeo Route Planner: Create Driver

Creates a new driver in Zeo Route Planner.

```
POST https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-driver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeo Route Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-driver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeoRoutePlanner/latest/actions/create-driver', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Driver address. |
| `email` | string | no | Driver email. |
| `name` | string | no | Name of the driver. |
| `password` | string | no | Password for the driver account. |
| `phoneNo` | string | no | Driver phone number. |

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
| `address` | string | Driver address. |
| `countryCodeName` | string | Phone country code name when available. |
| `email` | string | Driver email address. |
| `id` | number | Driver identifier. |
| `latitude` | number | Driver latitude when available. |
| `longitude` | number | Driver longitude when available. |
| `name` | string | Driver name. |
| `phoneNo` | string | Driver phone number. |
| `postalCode` | string | Postal code when available. |
| `vehicleType` | string | Assigned vehicle type when available. |

## Native endpoint

Through the native Zeo Route Planner API, this operation is `POST /api/v5/drivers` (base URL `https://zeorouteplanner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-driver.md) for the provider-specific parameters and requirements.

