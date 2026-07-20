# Viewneo: Update Device Group

Updates an existing device group in Viewneo.

```
PUT https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/update-device-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/update-device-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "displayAppProperties": 1,
  "isNotificationEnabled": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/update-device-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "displayAppProperties": 1,
    "isNotificationEnabled": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `name` | string | no |  |
| `displayAppProperties` | number | yes |  |
| `isNotificationEnabled` | number | yes |  |

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
      "interactiveWebsite": {},
      "isAlarmEnabled": 1,
      "isAnalyticsEnabled": 1,
      "isNotificationEnabled": 1,
      "isPinEnabled": 1,
      "isRs232Enabled": 1,
      "label": {},
      "left": {},
      "liveTicker": {},
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
| `interactiveWebsite` | object |  |
| `isAlarmEnabled` | number |  |
| `isAnalyticsEnabled` | number |  |
| `isNotificationEnabled` | number |  |
| `isPinEnabled` | number |  |
| `isRs232Enabled` | number |  |
| `label` | object |  |
| `left` | object |  |
| `liveTicker` | object |  |
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

Through the native Viewneo API, this operation is `POST /devicegroup/:id` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-device-group.md) for the provider-specific parameters and requirements.

