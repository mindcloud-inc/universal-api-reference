# Calibre: Create Test Profile

Creates a new test profile in Calibre.

```
POST https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-test-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-test-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.site": "string",
  "variables.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-test-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.site": "string",
    "variables.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.site` | string | yes | Site slug, found in site settings. |
| `variables.name` | string | yes | A descriptive name for the test profile. |
| `variables.device` | string | no | Device tag to emulate during tests. Default: `Desktop`. |
| `variables.connection` | string | no | Network throttling tag for the profile. Default: `cable`. |
| `variables.adBlockerIsEnabled` | boolean | no | Enable the ad blocker during tests. Default: `false`. |
| `variables.jsIsDisabled` | boolean | no | Disable JavaScript requests during the test. Default: `false`. |
| `variables.position` | number | no | Optional order position for the profile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTestProfile": {
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
| `createTestProfile.adBlockerIsEnabled` | boolean |  |
| `createTestProfile.bandwidth.tag` | string |  |
| `createTestProfile.bandwidth.title` | string |  |
| `createTestProfile.createdAt` | date |  |
| `createTestProfile.device.tag` | string |  |
| `createTestProfile.device.title` | string |  |
| `createTestProfile.jsIsDisabled` | boolean |  |
| `createTestProfile.name` | string |  |
| `createTestProfile.position` | number |  |
| `createTestProfile.updatedAt` | date |  |
| `createTestProfile.uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-test-profile.md) for the provider-specific parameters and requirements.

