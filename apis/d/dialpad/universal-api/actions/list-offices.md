# Dialpad: List Offices

Retrieves accessible office records from Dialpad.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-offices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-offices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-offices?${params}`, {
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
| `activeOnly` | boolean | no | Whether we only return active offices. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availabilityStatus": "string",
      "country": "string",
      "e911Address": {
        "address": "string",
        "address2": "string",
        "city": "string",
        "country": "string",
        "state": "string",
        "zip": "string"
      },
      "firstAction": "string",
      "fridayHours": [
        "string"
      ],
      "id": "string",
      "isPrimaryOffice": true,
      "mondayHours": [
        "string"
      ],
      "name": "Ava Chen",
      "noOperatorsAction": "string",
      "officeId": "string",
      "officeSettings": {
        "allowDeviceGuestLogin": true,
        "blockCallerIdDisabled": true,
        "bridgedTargetRecordingAllowed": true,
        "disableDeskPhoneSelfProvision": true,
        "disableIvrVoicemail": true,
        "noRecordingMessageOnUserCalls": true,
        "setCallerIdDisabled": true
      },
      "phoneNumbers": [
        "string"
      ],
      "ringSeconds": "string",
      "routingOptions": {
        "closed": {
          "action": "string",
          "dtmf": [
            {
              "input": "string",
              "options": {
                "action": "string"
              }
            }
          ],
          "operatorRouting": "string",
          "tryDialOperators": true
        },
        "open": {
          "action": "string",
          "dtmf": [
            {
              "input": "string",
              "options": {
                "action": "string"
              }
            }
          ],
          "operatorRouting": "string",
          "tryDialOperators": true
        }
      },
      "state": "string",
      "thursdayHours": [
        "string"
      ],
      "timezone": "string",
      "tuesdayHours": [
        "string"
      ],
      "wednesdayHours": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityStatus` | string |  |
| `country` | string |  |
| `e911Address.address` | string |  |
| `e911Address.address2` | string |  |
| `e911Address.city` | string |  |
| `e911Address.country` | string |  |
| `e911Address.state` | string |  |
| `e911Address.zip` | string |  |
| `firstAction` | string |  |
| `fridayHours[]` | string |  |
| `id` | string |  |
| `isPrimaryOffice` | boolean |  |
| `mondayHours[]` | string |  |
| `name` | string |  |
| `noOperatorsAction` | string |  |
| `officeId` | string |  |
| `officeSettings.allowDeviceGuestLogin` | boolean |  |
| `officeSettings.blockCallerIdDisabled` | boolean |  |
| `officeSettings.bridgedTargetRecordingAllowed` | boolean |  |
| `officeSettings.disableDeskPhoneSelfProvision` | boolean |  |
| `officeSettings.disableIvrVoicemail` | boolean |  |
| `officeSettings.noRecordingMessageOnUserCalls` | boolean |  |
| `officeSettings.setCallerIdDisabled` | boolean |  |
| `phoneNumbers[]` | string |  |
| `ringSeconds` | string |  |
| `routingOptions.closed.action` | string |  |
| `routingOptions.closed.dtmf[].input` | string |  |
| `routingOptions.closed.dtmf[].options.action` | string |  |
| `routingOptions.closed.operatorRouting` | string |  |
| `routingOptions.closed.tryDialOperators` | boolean |  |
| `routingOptions.open.action` | string |  |
| `routingOptions.open.dtmf[].input` | string |  |
| `routingOptions.open.dtmf[].options.action` | string |  |
| `routingOptions.open.operatorRouting` | string |  |
| `routingOptions.open.tryDialOperators` | boolean |  |
| `state` | string |  |
| `thursdayHours[]` | string |  |
| `timezone` | string |  |
| `tuesdayHours[]` | string |  |
| `wednesdayHours[]` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `GET /offices` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-offices.md) for the provider-specific parameters and requirements.

