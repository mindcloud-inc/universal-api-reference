# OneSignal Universal API Examples

These examples use the MindCloud API key and OneSignal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Messages

Retrieves messages from OneSignal.

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

Example response:

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

See the full [List Messages action reference](actions/list-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneSignal/latest/actions/list-messages).

## Create or Update Alias

Creates or updates a user alias in OneSignal.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-or-update-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "aliasId": "string",
  "aliasLabel": "string",
  "identity": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/create-or-update-alias', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "aliasId": "string",
    "aliasLabel": "string",
    "identity": {}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "identity": {
        "externalId": "string",
        "onesignalId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create or Update Alias action reference](actions/create-or-update-alias.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneSignal/latest/actions/create-or-update-alias).
