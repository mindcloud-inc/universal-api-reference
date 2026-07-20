# Xola: List Experiences

Finds experiences in Xola.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-experiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-experiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/list-experiences?${params}`, {
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
      "autoChargeOnDepositReminder": true,
      "balanceDueOffset": 1,
      "balanceDueReminder": true,
      "businessHours": "string",
      "category": "string",
      "complete": true,
      "currency": "string",
      "customerNamePreference": "Ava Chen",
      "cutoff": 1,
      "desc": "string",
      "duration": 1,
      "earlyReturn": true,
      "eventDuration": 1,
      "excerpt": "string",
      "geo": {
        "lat": 1,
        "lng": 1
      },
      "group": {
        "orderMax": 1,
        "orderMin": 1,
        "outingMax": 1,
        "outingMin": 1,
        "outingMinCutoff": 1
      },
      "guestType": "string",
      "id": "string",
      "isScheduled": true,
      "name": "Ava Chen",
      "paymentMethod": "string",
      "photo": {
        "id": "string",
        "src": "string",
        "type": "string"
      },
      "pickupAddress": "string",
      "pickupGeo": {
        "lat": 1,
        "lng": 1
      },
      "requireAdult": true,
      "requireGuestIdentification": true,
      "scheduleType": "string",
      "seller": {
        "id": "string"
      },
      "status": "string",
      "travelerPreference": {
        "allowPayment": {
          "value": true
        },
        "questionnaire": {
          "value": true
        }
      },
      "updated": "2026-05-07T12:00:00.000Z",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoChargeOnDepositReminder` | boolean |  |
| `balanceDueOffset` | number |  |
| `balanceDueReminder` | boolean |  |
| `businessHours` | string |  |
| `category` | string |  |
| `complete` | boolean |  |
| `currency` | string |  |
| `customerNamePreference` | string |  |
| `cutoff` | number |  |
| `desc` | string |  |
| `duration` | number |  |
| `earlyReturn` | boolean |  |
| `eventDuration` | number |  |
| `excerpt` | string |  |
| `geo.lat` | number |  |
| `geo.lng` | number |  |
| `group.orderMax` | number |  |
| `group.orderMin` | number |  |
| `group.outingMax` | number |  |
| `group.outingMin` | number |  |
| `group.outingMinCutoff` | number |  |
| `guestType` | string |  |
| `id` | string |  |
| `isScheduled` | boolean |  |
| `name` | string |  |
| `paymentMethod` | string |  |
| `photo.id` | string |  |
| `photo.src` | string |  |
| `photo.type` | string |  |
| `pickupAddress` | string |  |
| `pickupGeo.lat` | number |  |
| `pickupGeo.lng` | number |  |
| `requireAdult` | boolean |  |
| `requireGuestIdentification` | boolean |  |
| `scheduleType` | string |  |
| `seller.id` | string |  |
| `status` | string |  |
| `travelerPreference.allowPayment.value` | boolean |  |
| `travelerPreference.questionnaire.value` | boolean |  |
| `updated` | date |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Xola API, this operation is `GET /experiences` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-experiences.md) for the provider-specific parameters and requirements.

