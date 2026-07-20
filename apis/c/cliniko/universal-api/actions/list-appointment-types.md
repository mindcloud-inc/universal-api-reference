# Cliniko: List Appointment Types

Retrieves appointment types from your Cliniko account.

```
GET https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-appointment-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cliniko `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-appointment-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cliniko/latest/actions/list-appointment-types?${params}`, {
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
      "appointmentTypes": [
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
      "links": {
        "self": "https://example.com"
      },
      "totalEntries": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentTypes[].addDepositToAccountCredit` | object |  |
| `appointmentTypes[].appointmentConfirmationTemplateIds` | object |  |
| `appointmentTypes[].appointmentFollowUpTemplateIds` | object |  |
| `appointmentTypes[].appointmentReminderTemplateIds` | object |  |
| `appointmentTypes[].appointmentTypeBillableItems.links.self` | string |  |
| `appointmentTypes[].appointmentTypeProducts.links.self` | string |  |
| `appointmentTypes[].archivedAt` | object |  |
| `appointmentTypes[].billableItem.links.self` | string |  |
| `appointmentTypes[].category` | object |  |
| `appointmentTypes[].color` | string |  |
| `appointmentTypes[].createdAt` | string |  |
| `appointmentTypes[].depositPrice` | object |  |
| `appointmentTypes[].description` | object |  |
| `appointmentTypes[].durationInMinutes` | number |  |
| `appointmentTypes[].id` | string |  |
| `appointmentTypes[].links.self` | string |  |
| `appointmentTypes[].maxAttendees` | number |  |
| `appointmentTypes[].name` | string |  |
| `appointmentTypes[].onlineBookingsLeadTimeHours` | object |  |
| `appointmentTypes[].onlinePaymentsEnabled` | boolean |  |
| `appointmentTypes[].onlinePaymentsMode` | object |  |
| `appointmentTypes[].practitioners.links.self` | string |  |
| `appointmentTypes[].showInOnlineBookings` | boolean |  |
| `appointmentTypes[].telehealthEnabled` | boolean |  |
| `appointmentTypes[].updatedAt` | string |  |
| `links.self` | string |  |
| `totalEntries` | number |  |

## Native endpoint

Through the native Cliniko API, this operation is `GET /appointment_types` (base URL `https://api.au5.cliniko.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-appointment-types.md) for the provider-specific parameters and requirements.

