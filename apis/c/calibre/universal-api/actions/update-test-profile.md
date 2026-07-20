# Calibre: Update Test Profile

Updates an existing test profile in Calibre.

```
PUT https://connect.mindcloud.co/v1/universal/calibre/latest/actions/update-test-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/update-test-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.site": "string",
  "variables.uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/update-test-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.site": "string",
    "variables.uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.site` | string | yes | Site slug, found in site settings. |
| `variables.uuid` | string | yes | UUID of the test profile to update. |
| `variables.name` | string | no | A descriptive name for the test profile. |
| `variables.device` | string | no | Device tag to emulate during tests. |
| `variables.connection` | string | no | Network throttling tag for the profile. |
| `variables.adBlockerIsEnabled` | boolean | no | Enable the ad blocker during tests. |
| `variables.jsIsDisabled` | boolean | no | Disable JavaScript requests during the test. |
| `variables.position` | number | no | Optional order position for the profile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updateTestProfile": {
        "adBlockerIsEnabled": true,
        "bandwidth": {
          "tag": "string",
          "title": "string"
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "device": {
          "tag": "string",
          "title": "string"
        },
        "jsIsDisabled": true,
        "name": "Ava Chen",
        "position": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updateTestProfile.adBlockerIsEnabled` | boolean |  |
| `updateTestProfile.bandwidth.tag` | string |  |
| `updateTestProfile.bandwidth.title` | string |  |
| `updateTestProfile.createdAt` | date |  |
| `updateTestProfile.device.tag` | string |  |
| `updateTestProfile.device.title` | string |  |
| `updateTestProfile.jsIsDisabled` | boolean |  |
| `updateTestProfile.name` | string |  |
| `updateTestProfile.position` | number |  |
| `updateTestProfile.updatedAt` | date |  |
| `updateTestProfile.uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-test-profile.md) for the provider-specific parameters and requirements.

