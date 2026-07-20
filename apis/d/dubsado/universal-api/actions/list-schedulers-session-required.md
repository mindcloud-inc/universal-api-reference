# Dubsado: List Schedulers (Session Required)



```
GET https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-schedulers-session-required
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubsado `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-schedulers-session-required?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/list-schedulers-session-required?${params}`, {
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
| `projectId` | string | no | Optional project ID filter observed in the Dubsado app bundle for /scheduler reads. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apptAvailability": {
        "daysRolling": 1,
        "value": "string"
      },
      "bookedCount": 1,
      "brand": "string",
      "buffer": {
        "after": 1,
        "before": 1
      },
      "description": "string",
      "duration": {
        "timeSpan": "string",
        "value": 1
      },
      "emailTemplate": {
        "body": "ava@example.com",
        "subject": "ava@example.com"
      },
      "index": 1,
      "invoiceSettings": {
        "invoice": {
          "items": [
            {
              "price": 1,
              "quantity": 1
            }
          ],
          "number": 1
        },
        "requireDeposit": true
      },
      "isMonthlyView": true,
      "location": "string",
      "maxBookings": 1,
      "maxPerDay": 1,
      "notifications": {
        "bccMe": true,
        "reminders": [
          {
            "subject": "string",
            "template": "string",
            "timeSpan": "string",
            "value": 1
          }
        ],
        "sendReminders": true
      },
      "preventBooking": 1,
      "prohibitReschedule": true,
      "schedulerDates": [
        {
          "syncAll": true,
          "unavailable": true,
          "weekday": "string"
        }
      ],
      "sent": true,
      "timeIncrement": 1,
      "timeIncrementUnit": "string",
      "title": "string",
      "transparency": "string",
      "welcomeMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apptAvailability.daysRolling` | number |  |
| `apptAvailability.value` | string |  |
| `bookedCount` | number |  |
| `brand` | string |  |
| `buffer.after` | number |  |
| `buffer.before` | number |  |
| `description` | string |  |
| `duration.timeSpan` | string |  |
| `duration.value` | number |  |
| `emailTemplate.body` | string |  |
| `emailTemplate.subject` | string |  |
| `index` | number |  |
| `invoiceSettings.invoice.items[].price` | number |  |
| `invoiceSettings.invoice.items[].quantity` | number |  |
| `invoiceSettings.invoice.number` | number |  |
| `invoiceSettings.requireDeposit` | boolean |  |
| `isMonthlyView` | boolean |  |
| `location` | string |  |
| `maxBookings` | number |  |
| `maxPerDay` | number |  |
| `notifications.bccMe` | boolean |  |
| `notifications.reminders[].subject` | string |  |
| `notifications.reminders[].template` | string |  |
| `notifications.reminders[].timeSpan` | string |  |
| `notifications.reminders[].value` | number |  |
| `notifications.sendReminders` | boolean |  |
| `preventBooking` | number |  |
| `prohibitReschedule` | boolean |  |
| `schedulerDates[].syncAll` | boolean |  |
| `schedulerDates[].unavailable` | boolean |  |
| `schedulerDates[].weekday` | string |  |
| `sent` | boolean |  |
| `timeIncrement` | number |  |
| `timeIncrementUnit` | string |  |
| `title` | string |  |
| `transparency` | string |  |
| `welcomeMsg` | string |  |

## Native endpoint

Through the native Dubsado API, this operation is `GET /scheduler` (base URL `https://app.dubsado.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedulers-session-required.md) for the provider-specific parameters and requirements.

