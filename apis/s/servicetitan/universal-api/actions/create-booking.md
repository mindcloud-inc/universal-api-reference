# ServiceTitan: Create Booking



```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "summary": "string",
  "name": "Ava Chen",
  "externalId": "string",
  "isFirstTimeClient": true,
  "source": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-booking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "summary": "string",
    "name": "Ava Chen",
    "externalId": "string",
    "isFirstTimeClient": true,
    "source": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address.city` | string | no |  |
| `address.state` | string | no |  |
| `address.zip` | string | no |  |
| `address.street` | string | no |  |
| `contacts[].type` | string | no | Phone , Phone , Email , Fax , MobilePhone |
| `summary` | string | yes |  |
| `address.unit` | string | no |  |
| `contacts[].value` | string | no |  |
| `name` | string | yes |  |
| `contacts[].memo` | string | no |  |
| `externalId` | string | yes |  |
| `isFirstTimeClient` | boolean | yes |  |
| `source` | string | yes |  |
| `address.country` | string | no | Default: `US`. |
| `phone` | string | no |  |
| `email` | string | no |  |
| `address` | object | no |  |
| `contacts[]` | array | no |  |
| `customerType` | string | no |  |
| `start` | string | no |  |
| `priority` | object | no |  |
| `uploadedImages` | array | no |  |
| `isSendConfirmationEmail` | boolean | no |  |
| `bookingProviderId` | list | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST crm/v2/tenant/{{credentials.tenant}}/booking-provider/:bookingProviderId/bookings` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking.md) for the provider-specific parameters and requirements.

