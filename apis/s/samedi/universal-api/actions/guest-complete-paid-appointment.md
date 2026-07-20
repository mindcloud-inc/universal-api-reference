# Samedi: Guest Complete Paid Appointment

Completes a paid appointment booking in Samedi for a guest.

```
POST https://connect.mindcloud.co/v1/universal/samedi/latest/actions/guest-complete-paid-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samedi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/samedi/latest/actions/guest-complete-paid-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderUrl": "https://example.com",
  "billingInformation.firstName": "Ava",
  "billingInformation.lastName": "Chen",
  "billingInformation.street": "string",
  "billingInformation.city": "string",
  "billingInformation.country": "string",
  "billingInformation.zip": "string",
  "billingInformation.email": "ava@example.com",
  "eventCategoryId": "string",
  "eventTypeId": "string",
  "startsAt": "string",
  "attendant.data.firstName": "Ava",
  "attendant.data.lastName": "Chen",
  "attendant.data.email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samedi/latest/actions/guest-complete-paid-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderUrl": "https://example.com",
    "billingInformation.firstName": "Ava",
    "billingInformation.lastName": "Chen",
    "billingInformation.street": "string",
    "billingInformation.city": "string",
    "billingInformation.country": "string",
    "billingInformation.zip": "string",
    "billingInformation.email": "ava@example.com",
    "eventCategoryId": "string",
    "eventTypeId": "string",
    "startsAt": "string",
    "attendant.data.firstName": "Ava",
    "attendant.data.lastName": "Chen",
    "attendant.data.email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderUrl` | string | yes | PayPal order URL in the documented samedi format. |
| `billingInformation.firstName` | string | yes | Billing first name. |
| `billingInformation.lastName` | string | yes | Billing last name. |
| `billingInformation.street` | string | yes | Billing street address. |
| `billingInformation.city` | string | yes | Billing city. |
| `billingInformation.country` | string | yes | Billing country as ISO 3166-1 alpha-2 code. |
| `billingInformation.zip` | string | yes | Billing ZIP or postal code. |
| `billingInformation.email` | string | yes | Billing email address. |
| `eventCategoryId` | string | yes | Appointment category ID for the guest paid booking. |
| `eventTypeId` | string | yes | Appointment type ID for the guest paid booking. |
| `startsAt` | string | yes | Selected appointment start timestamp for the guest paid booking. |
| `attendant.data.firstName` | string | yes | Patient first name for guest booking. |
| `attendant.data.lastName` | string | yes | Patient last name for guest booking. |
| `attendant.data.email` | string | yes | Patient email for guest booking. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `doNotification` | boolean | no | Legacy consent flag that enables or disables both email and SMS notifications. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samedi API returns.

## Native endpoint

Through the native Samedi API, this operation is `POST /booking/v3/book` (base URL `https://patient.samedi.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/guest-complete-paid-appointment.md) for the provider-specific parameters and requirements.

