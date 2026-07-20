# Seam: Get Device

Retrieves a device from Seam by ID or name.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-device
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-device?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-device?${params}`, {
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
| `deviceId` | string | no | ID of the device that you want to get. |
| `name` | string | no | Name of the device that you want to get. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canProgramOnlineAccessCodes": true,
      "canRemotelyUnlock": true,
      "canUnlockWithCode": true,
      "capabilitiesSupported": [
        "string"
      ],
      "connectedAccountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customMetadata": {},
      "deviceId": "string",
      "deviceManufacturer": {},
      "deviceProvider": {},
      "deviceType": "string",
      "displayName": "Ava Chen",
      "errors": [
        {}
      ],
      "isManaged": true,
      "location": {},
      "nickname": "Ava Chen",
      "properties": {},
      "spaceIds": [
        "string"
      ],
      "warnings": [
        {}
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canProgramOnlineAccessCodes` | boolean |  |
| `canRemotelyUnlock` | boolean |  |
| `canUnlockWithCode` | boolean |  |
| `capabilitiesSupported` | array<string> |  |
| `connectedAccountId` | string |  |
| `createdAt` | date |  |
| `customMetadata` | object |  |
| `deviceId` | string |  |
| `deviceManufacturer` | object |  |
| `deviceProvider` | object |  |
| `deviceType` | string |  |
| `displayName` | string |  |
| `errors` | array<object> |  |
| `isManaged` | boolean |  |
| `location` | object |  |
| `nickname` | string |  |
| `properties` | object |  |
| `spaceIds` | array<string> |  |
| `warnings` | array<object> |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Seam API, this operation is `POST /devices/get` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device.md) for the provider-specific parameters and requirements.

