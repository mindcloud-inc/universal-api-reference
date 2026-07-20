# Viewneo: Delete Device Group

Deletes an existing device group from Viewneo.

```
DELETE https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/delete-device-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/delete-device-group?connectionId=$CONNECTION_ID&id=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/delete-device-group?${params}`, {
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
| `id` | number | yes |  |
| `id` | number | yes | ID of deviceGroup |

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
      "deletedAt": "string",
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
      "mediafileIdAsInteractionWebsite": {},
      "name": "Ava Chen",
      "notifyAfter": {},
      "notifyByEmail": {},
      "pin": {},
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
| `deletedAt` | string |  |
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
| `mediafileIdAsInteractionWebsite` | object |  |
| `name` | string |  |
| `notifyAfter` | object |  |
| `notifyByEmail` | object |  |
| `pin` | object |  |
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

Through the native Viewneo API, this operation is `DELETE /devicegroup/:id` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-device-group.md) for the provider-specific parameters and requirements.

