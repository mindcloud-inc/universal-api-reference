# Cliniko: Get Appointment Type

Retrieves an appointment type from your Cliniko account.

```
GET https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-appointment-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliniko `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-appointment-type?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/get-appointment-type?${params}`, {
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
| `id` | string | yes | The Cliniko appointment type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addDepositToAccountCredit": {},
      "appointmentConfirmationTemplateIds": {},
      "appointmentFollowUpTemplateIds": {},
      "appointmentReminderTemplateIds": {},
      "appointmentTypeBillableItems": {
        "links": {
          "self": "https://example.com"
        }
      },
      "appointmentTypeProducts": {
        "links": {
          "self": "https://example.com"
        }
      },
      "archivedAt": {},
      "billableItem": {
        "links": {
          "self": "https://example.com"
        }
      },
      "category": {},
      "color": "string",
      "createdAt": "string",
      "depositPrice": {},
      "description": {},
      "durationInMinutes": 1,
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "maxAttendees": 1,
      "name": "Ava Chen",
      "onlineBookingsLeadTimeHours": {},
      "onlinePaymentsEnabled": true,
      "onlinePaymentsMode": {},
      "practitioners": {
        "links": {
          "self": "https://example.com"
        }
      },
      "showInOnlineBookings": true,
      "telehealthEnabled": true,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addDepositToAccountCredit` | object |  |
| `appointmentConfirmationTemplateIds` | object |  |
| `appointmentFollowUpTemplateIds` | object |  |
| `appointmentReminderTemplateIds` | object |  |
| `appointmentTypeBillableItems.links.self` | string |  |
| `appointmentTypeProducts.links.self` | string |  |
| `archivedAt` | object |  |
| `billableItem.links.self` | string |  |
| `category` | object |  |
| `color` | string |  |
| `createdAt` | string |  |
| `depositPrice` | object |  |
| `description` | object |  |
| `durationInMinutes` | number |  |
| `id` | string |  |
| `links.self` | string |  |
| `maxAttendees` | number |  |
| `name` | string |  |
| `onlineBookingsLeadTimeHours` | object |  |
| `onlinePaymentsEnabled` | boolean |  |
| `onlinePaymentsMode` | object |  |
| `practitioners.links.self` | string |  |
| `showInOnlineBookings` | boolean |  |
| `telehealthEnabled` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Cliniko API, this operation is `GET /appointment_types/:id` (base URL `https://api.au5.cliniko.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-appointment-type.md) for the provider-specific parameters and requirements.

