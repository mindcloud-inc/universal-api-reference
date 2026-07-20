# Viewneo: List Device Groups

Retrieves all device groups from Viewneo.

```
GET https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-device-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-device-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/list-device-groups?${params}`, {
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
      "alarmSensibility": 1,
      "channelLogoDisplayPosition": {},
      "channelLogoId": {},
      "channelLogoOpacity": {},
      "comment": "string",
      "companyId": 1,
      "createdAt": "string",
      "deletedAt": {},
      "displayAppProperties": 1,
      "height": {},
      "id": 1,
      "interactionEnabled": 1,
      "interactionTimeout": 1,
      "isAlarmEnabled": 1,
      "isAnalyticsEnabled": 1,
      "isNotificationEnabled": 1,
      "isPinEnabled": 1,
      "isRs232Enabled": 1,
      "label": {},
      "left": {},
      "liveTicker": {
        "backgroundColor": "string",
        "clockFormat": 1,
        "clockPosition": 1,
        "color": "string",
        "companyId": 1,
        "createdAt": "string",
        "deletedAt": {},
        "deviceGroupId": 1,
        "deviceId": {},
        "direction": 1,
        "displayPosition": 1,
        "id": 1,
        "isActive": 1,
        "isClockActive": 1,
        "rssFeed": "string",
        "speed": 1,
        "text": "string",
        "updatedAt": "string"
      },
      "mediafileIdAsInteractionWebsite": {},
      "multiFrame": {},
      "name": "Ava Chen",
      "notifyAfter": {},
      "notifyByEmail": {},
      "pin": {},
      "playlist": {
        "comment": "string",
        "companyId": 1,
        "createdAt": "string",
        "deletedAt": {},
        "id": 1,
        "isAdvertised": 1,
        "isDefault": 1,
        "isDemo": 1,
        "isShared": 1,
        "label": {},
        "name": "Ava Chen",
        "numberOfEntries": 1,
        "playbackEntryCount": 1,
        "playbackOrder": 1,
        "playbackRule": 1,
        "type": 1,
        "updatedAt": "string"
      },
      "playlistId": 1,
      "rotation": 1,
      "rs232Baud": 1,
      "rs232DataBits": 1,
      "rs232DisplayOff": "string",
      "rs232DisplayOn": "string",
      "rs232Format": 1,
      "rs232Parity": 1,
      "rs232StopBits": 1,
      "screenScale": 1,
      "timezone": "string",
      "top": {},
      "type": 1,
      "updatedAt": "string",
      "updateInterval": 1,
      "updateIntervalSetting": 1,
      "volume": 1,
      "width": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alarmSensibility` | number |  |
| `channelLogoDisplayPosition` | object |  |
| `channelLogoId` | object |  |
| `channelLogoOpacity` | object |  |
| `comment` | string |  |
| `companyId` | number |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `displayAppProperties` | number |  |
| `height` | object |  |
| `id` | number |  |
| `interactionEnabled` | number |  |
| `interactionTimeout` | number |  |
| `isAlarmEnabled` | number |  |
| `isAnalyticsEnabled` | number |  |
| `isNotificationEnabled` | number |  |
| `isPinEnabled` | number |  |
| `isRs232Enabled` | number |  |
| `label` | object |  |
| `left` | object |  |
| `liveTicker.backgroundColor` | string |  |
| `liveTicker.clockFormat` | number |  |
| `liveTicker.clockPosition` | number |  |
| `liveTicker.color` | string |  |
| `liveTicker.companyId` | number |  |
| `liveTicker.createdAt` | string |  |
| `liveTicker.deletedAt` | object |  |
| `liveTicker.deviceGroupId` | number |  |
| `liveTicker.deviceId` | object |  |
| `liveTicker.direction` | number |  |
| `liveTicker.displayPosition` | number |  |
| `liveTicker.id` | number |  |
| `liveTicker.isActive` | number |  |
| `liveTicker.isClockActive` | number |  |
| `liveTicker.rssFeed` | string |  |
| `liveTicker.speed` | number |  |
| `liveTicker.text` | string |  |
| `liveTicker.updatedAt` | string |  |
| `mediafileIdAsInteractionWebsite` | object |  |
| `multiFrame` | object |  |
| `name` | string |  |
| `notifyAfter` | object |  |
| `notifyByEmail` | object |  |
| `pin` | object |  |
| `playlist.comment` | string |  |
| `playlist.companyId` | number |  |
| `playlist.createdAt` | string |  |
| `playlist.deletedAt` | object |  |
| `playlist.id` | number |  |
| `playlist.isAdvertised` | number |  |
| `playlist.isDefault` | number |  |
| `playlist.isDemo` | number |  |
| `playlist.isShared` | number |  |
| `playlist.label` | object |  |
| `playlist.name` | string |  |
| `playlist.numberOfEntries` | number |  |
| `playlist.playbackEntryCount` | number |  |
| `playlist.playbackOrder` | number |  |
| `playlist.playbackRule` | number |  |
| `playlist.type` | number |  |
| `playlist.updatedAt` | string |  |
| `playlistId` | number |  |
| `rotation` | number |  |
| `rs232Baud` | number |  |
| `rs232DataBits` | number |  |
| `rs232DisplayOff` | string |  |
| `rs232DisplayOn` | string |  |
| `rs232Format` | number |  |
| `rs232Parity` | number |  |
| `rs232StopBits` | number |  |
| `screenScale` | number |  |
| `timezone` | string |  |
| `top` | object |  |
| `type` | number |  |
| `updatedAt` | string |  |
| `updateInterval` | number |  |
| `updateIntervalSetting` | number |  |
| `volume` | number |  |
| `width` | object |  |

## Native endpoint

Through the native Viewneo API, this operation is `GET /devicegroup` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-device-groups.md) for the provider-specific parameters and requirements.

