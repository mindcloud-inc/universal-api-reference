# AntsRoute: Create Customer

Creates a new customer in AntsRoute.

```
POST https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AntsRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string",
  "lastName": "Chen",
  "latitude": 1,
  "longitude": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string",
    "lastName": "Chen",
    "latitude": 1,
    "longitude": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | Address of the customer |
| `comments` | string | no | Customer comments. |
| `email` | string | no | Customer email address. |
| `externalId` | string | no | External customer ID. |
| `firstName` | string | no | First name of the customer |
| `lastName` | string | yes | Last name of the customer |
| `latitude` | number | yes | Location latitude of the customer |
| `longitude` | number | yes | Location longitude of the customer |
| `mobileNumber` | string | no | Customer mobile number. |
| `openingHoursAlwaysOpen` | boolean | no | Whether the customer is always open. |
| `parkingTimeInMinutes` | number | no | Parking time in minutes. |
| `phoneNumber` | string | no | Customer phone number. |
| `skills[]` | array<string> | no | Required customer skills. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AntsRoute API returns.

## Native endpoint

Through the native AntsRoute API, this operation is `POST /capi/customer` (base URL `https://app.antsroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

