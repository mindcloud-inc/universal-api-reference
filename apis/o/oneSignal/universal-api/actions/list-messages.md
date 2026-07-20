# OneSignal: List Messages

Retrieves messages from OneSignal.

```
GET https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSignal `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/list-messages?${params}`, {
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
      "admBigPicture": {},
      "admGroup": {},
      "admLargeIcon": {},
      "admSmallIcon": {},
      "admSound": {},
      "alexaDisplayTitle": {},
      "alexaSsml": {},
      "amazonBackgroundData": {},
      "androidAccentColor": {},
      "androidChannelId": {},
      "androidGroup": {},
      "androidGroupMessage": {},
      "androidLedColor": {},
      "androidSound": {},
      "androidVisibility": {},
      "apnsAlert": {},
      "appId": "string",
      "appUrl": {},
      "bigPicture": {},
      "buttons": {},
      "canceled": true,
      "chromeBigPicture": {},
      "chromeIcon": {},
      "chromeWebBadge": {},
      "chromeWebIcon": {},
      "chromeWebImage": {},
      "completedAt": "2026-05-07T12:00:00.000Z",
      "contentAvailable": {},
      "converted": 1,
      "data": {},
      "delayedOption": {},
      "deliveryTimeOfDay": {},
      "emailClickTrackingDisabled": true,
      "emailFromAddress": "ava@example.com",
      "emailFromName": "ava@example.com",
      "emailPreheader": "ava@example.com",
      "emailReplyToAddress": "ava@example.com",
      "emailSubject": "ava@example.com",
      "errored": 1,
      "failed": 1,
      "fcapGroupIds": {},
      "fcapStatus": "string",
      "filters": {},
      "firefoxIcon": {},
      "globalImage": {},
      "huaweiAccentColor": {},
      "huaweiBadgeAddNum": {},
      "huaweiBadgeClass": {},
      "huaweiBadgeSetNum": {},
      "huaweiBigPicture": {},
      "huaweiBiTag": {},
      "huaweiCategory": {},
      "huaweiChannelId": {},
      "huaweiExistingChannelId": {},
      "huaweiGroup": {},
      "huaweiGroupMessage": {},
      "huaweiLargeIcon": {},
      "huaweiLedColor": {},
      "huaweiMsgType": {},
      "huaweiSmallIcon": {},
      "huaweiSound": {},
      "huaweiVisibility": "string",
      "id": "string",
      "includeAliases": {},
      "includedSegments": [
        "string"
      ],
      "includeExternalUserIds": {},
      "includePlayerIds": [
        "string"
      ],
      "includeUnsubscribed": true,
      "influencedOpens": 1,
      "iosAttachments": {},
      "iosBadgeCount": {},
      "iosBadgeType": {},
      "iosCategory": {},
      "iosInterruptionLevel": {},
      "iosRelevanceScore": {},
      "iosSound": {},
      "isAdm": true,
      "isAlexa": {},
      "isAndroid": true,
      "isChrome": true,
      "isChromeWeb": true,
      "isEdge": true,
      "isEmail": true,
      "isFirefox": true,
      "isHuawei": true,
      "isIos": true,
      "isSafari": true,
      "isSMS": true,
      "isWP": true,
      "isWPWNS": true,
      "largeIcon": {},
      "name": "Ava Chen",
      "platformDeliveryStats": {
        "email": {
          "bounced": 1,
          "clicks": 1,
          "converted": 1,
          "errored": 1,
          "failed": 1,
          "opened": 1,
          "received": 1,
          "reportedSpam": 1,
          "successful": 1,
          "suppressed": 1,
          "uniqueClicks": 1,
          "uniqueOpens": 1,
          "unsubscribed": 1
        }
      },
      "priority": 1,
      "queuedAt": "2026-05-07T12:00:00.000Z",
      "received": 1,
      "remaining": 1,
      "sendAfter": "2026-05-07T12:00:00.000Z",
      "smallIcon": {},
      "smsFrom": {},
      "smsMediaUrls": {},
      "spokenText": {},
      "subtitle": {},
      "successful": 1,
      "tags": {},
      "targetContentIdentifier": {},
      "templateId": {},
      "threadId": {},
      "throttleRatePerMinute": {},
      "ttl": 1,
      "url": {},
      "webButtons": {},
      "webPushTopic": {},
      "webUrl": {},
      "wpSound": {},
      "wpWnsSound": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admBigPicture` | object |  |
| `admGroup` | object |  |
| `admLargeIcon` | object |  |
| `admSmallIcon` | object |  |
| `admSound` | object |  |
| `alexaDisplayTitle` | object |  |
| `alexaSsml` | object |  |
| `amazonBackgroundData` | object |  |
| `androidAccentColor` | object |  |
| `androidChannelId` | object |  |
| `androidGroup` | object |  |
| `androidGroupMessage` | object |  |
| `androidLedColor` | object |  |
| `androidSound` | object |  |
| `androidVisibility` | object |  |
| `apnsAlert` | object |  |
| `appId` | string |  |
| `appUrl` | object |  |
| `bigPicture` | object |  |
| `buttons` | object |  |
| `canceled` | boolean |  |
| `chromeBigPicture` | object |  |
| `chromeIcon` | object |  |
| `chromeWebBadge` | object |  |
| `chromeWebIcon` | object |  |
| `chromeWebImage` | object |  |
| `completedAt` | date |  |
| `contentAvailable` | object |  |
| `converted` | number |  |
| `data` | object |  |
| `delayedOption` | object |  |
| `deliveryTimeOfDay` | object |  |
| `emailClickTrackingDisabled` | boolean |  |
| `emailFromAddress` | string |  |
| `emailFromName` | string |  |
| `emailPreheader` | string |  |
| `emailReplyToAddress` | string |  |
| `emailSubject` | string |  |
| `errored` | number |  |
| `failed` | number |  |
| `fcapGroupIds` | object |  |
| `fcapStatus` | string |  |
| `filters` | object |  |
| `firefoxIcon` | object |  |
| `globalImage` | object |  |
| `huaweiAccentColor` | object |  |
| `huaweiBadgeAddNum` | object |  |
| `huaweiBadgeClass` | object |  |
| `huaweiBadgeSetNum` | object |  |
| `huaweiBigPicture` | object |  |
| `huaweiBiTag` | object |  |
| `huaweiCategory` | object |  |
| `huaweiChannelId` | object |  |
| `huaweiExistingChannelId` | object |  |
| `huaweiGroup` | object |  |
| `huaweiGroupMessage` | object |  |
| `huaweiLargeIcon` | object |  |
| `huaweiLedColor` | object |  |
| `huaweiMsgType` | object |  |
| `huaweiSmallIcon` | object |  |
| `huaweiSound` | object |  |
| `huaweiVisibility` | string |  |
| `id` | string |  |
| `includeAliases` | object |  |
| `includedSegments[]` | string |  |
| `includeExternalUserIds` | object |  |
| `includePlayerIds[]` | string |  |
| `includeUnsubscribed` | boolean |  |
| `influencedOpens` | number |  |
| `iosAttachments` | object |  |
| `iosBadgeCount` | object |  |
| `iosBadgeType` | object |  |
| `iosCategory` | object |  |
| `iosInterruptionLevel` | object |  |
| `iosRelevanceScore` | object |  |
| `iosSound` | object |  |
| `isAdm` | boolean |  |
| `isAlexa` | object |  |
| `isAndroid` | boolean |  |
| `isChrome` | boolean |  |
| `isChromeWeb` | boolean |  |
| `isEdge` | boolean |  |
| `isEmail` | boolean |  |
| `isFirefox` | boolean |  |
| `isHuawei` | boolean |  |
| `isIos` | boolean |  |
| `isSafari` | boolean |  |
| `isSMS` | boolean |  |
| `isWP` | boolean |  |
| `isWPWNS` | boolean |  |
| `largeIcon` | object |  |
| `name` | string |  |
| `platformDeliveryStats.email.bounced` | number |  |
| `platformDeliveryStats.email.clicks` | number |  |
| `platformDeliveryStats.email.converted` | number |  |
| `platformDeliveryStats.email.errored` | number |  |
| `platformDeliveryStats.email.failed` | number |  |
| `platformDeliveryStats.email.opened` | number |  |
| `platformDeliveryStats.email.received` | number |  |
| `platformDeliveryStats.email.reportedSpam` | number |  |
| `platformDeliveryStats.email.successful` | number |  |
| `platformDeliveryStats.email.suppressed` | number |  |
| `platformDeliveryStats.email.uniqueClicks` | number |  |
| `platformDeliveryStats.email.uniqueOpens` | number |  |
| `platformDeliveryStats.email.unsubscribed` | number |  |
| `priority` | number |  |
| `queuedAt` | date |  |
| `received` | number |  |
| `remaining` | number |  |
| `sendAfter` | date |  |
| `smallIcon` | object |  |
| `smsFrom` | object |  |
| `smsMediaUrls` | object |  |
| `spokenText` | object |  |
| `subtitle` | object |  |
| `successful` | number |  |
| `tags` | object |  |
| `targetContentIdentifier` | object |  |
| `templateId` | object |  |
| `threadId` | object |  |
| `throttleRatePerMinute` | object |  |
| `ttl` | number |  |
| `url` | object |  |
| `webButtons` | object |  |
| `webPushTopic` | object |  |
| `webUrl` | object |  |
| `wpSound` | object |  |
| `wpWnsSound` | object |  |

## Native endpoint

Through the native OneSignal API, this operation is `GET /notifications` (base URL `https://api.onesignal.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

