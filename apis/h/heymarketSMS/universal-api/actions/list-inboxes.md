# Heymarket SMS: List Inboxes



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-inboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-inboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/list-inboxes?${params}`, {
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
      "aiAgentAutoAssign": true,
      "autoAssignable": true,
      "autoClose": true,
      "bcoChats": true,
      "businessHours": {
        "isWeekdayHoursSet": true,
        "isWeekendHoursSet": true,
        "quietHoursEnabled": true,
        "weekdayEndHour": 1,
        "weekdayEndMin": 1,
        "weekdayStartHour": 1,
        "weekdayStartMin": 1,
        "weekendEndHour": 1,
        "weekendEndMin": 1,
        "weekendStartHour": 1,
        "weekendStartMin": 1
      },
      "createdAt": "string",
      "emailOnInboundIdle": true,
      "emailOnOutboundIdle": true,
      "forceAssign": true,
      "highThroughput": true,
      "id": 1,
      "ignoreIncCallNotif": true,
      "isBandwidth": true,
      "isBusinessHours": true,
      "isQuietHours": true,
      "ittc": 1,
      "members": [
        1
      ],
      "name": "Ava Chen",
      "notifyAfterInboundIdle": 1,
      "notifyAfterOutboundIdle": 1,
      "notifyAll": true,
      "notifyOnChatAssignment": true,
      "notifyOnInboundIdle": true,
      "notifyOnOutboundIdle": true,
      "promoteInboundIdleToTop": true,
      "promoteOutboundIdleToTop": true,
      "rev": 1,
      "showWaitingIndicator": true,
      "team": 1,
      "unassignOnClose": true,
      "updatedAt": "string",
      "widgetSettings": {
        "emailEnabled": true,
        "emailRequired": true,
        "nameEnabled": true,
        "nameRequired": true,
        "phoneEnabled": true,
        "phoneOptional": true,
        "smsDisabled": true,
        "webchatEnabled": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiAgentAutoAssign` | boolean |  |
| `autoAssignable` | boolean |  |
| `autoClose` | boolean |  |
| `bcoChats` | boolean |  |
| `businessHours.isWeekdayHoursSet` | boolean |  |
| `businessHours.isWeekendHoursSet` | boolean |  |
| `businessHours.quietHoursEnabled` | boolean |  |
| `businessHours.weekdayEndHour` | number |  |
| `businessHours.weekdayEndMin` | number |  |
| `businessHours.weekdayStartHour` | number |  |
| `businessHours.weekdayStartMin` | number |  |
| `businessHours.weekendEndHour` | number |  |
| `businessHours.weekendEndMin` | number |  |
| `businessHours.weekendStartHour` | number |  |
| `businessHours.weekendStartMin` | number |  |
| `createdAt` | string |  |
| `emailOnInboundIdle` | boolean |  |
| `emailOnOutboundIdle` | boolean |  |
| `forceAssign` | boolean |  |
| `highThroughput` | boolean |  |
| `id` | number |  |
| `ignoreIncCallNotif` | boolean |  |
| `isBandwidth` | boolean |  |
| `isBusinessHours` | boolean |  |
| `isQuietHours` | boolean |  |
| `ittc` | number |  |
| `members[]` | number |  |
| `name` | string |  |
| `notifyAfterInboundIdle` | number |  |
| `notifyAfterOutboundIdle` | number |  |
| `notifyAll` | boolean |  |
| `notifyOnChatAssignment` | boolean |  |
| `notifyOnInboundIdle` | boolean |  |
| `notifyOnOutboundIdle` | boolean |  |
| `promoteInboundIdleToTop` | boolean |  |
| `promoteOutboundIdleToTop` | boolean |  |
| `rev` | number |  |
| `showWaitingIndicator` | boolean |  |
| `team` | number |  |
| `unassignOnClose` | boolean |  |
| `updatedAt` | string |  |
| `widgetSettings.emailEnabled` | boolean |  |
| `widgetSettings.emailRequired` | boolean |  |
| `widgetSettings.nameEnabled` | boolean |  |
| `widgetSettings.nameRequired` | boolean |  |
| `widgetSettings.phoneEnabled` | boolean |  |
| `widgetSettings.phoneOptional` | boolean |  |
| `widgetSettings.smsDisabled` | boolean |  |
| `widgetSettings.webchatEnabled` | boolean |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `GET /v1/inboxes` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inboxes.md) for the provider-specific parameters and requirements.

