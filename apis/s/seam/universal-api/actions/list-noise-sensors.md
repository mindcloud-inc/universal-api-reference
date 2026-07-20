# Seam: List Noise Sensors

Retrieves a list of noise sensors from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-noise-sensors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-noise-sensors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-noise-sensors?${params}`, {
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
| `connectedAccountId` | string | no | ID of the connected account for which you want to list noise sensors. |
| `search` | string | no | Search string for noise sensors. |
| `spaceId` | string | no | ID of the space for which you want to list noise sensors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilitiesSupported": [
        "string"
      ],
      "connectedAccountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customMetadata": {},
      "deviceId": "string",
      "deviceType": "string",
      "displayName": "Ava Chen",
      "errors": [
        {}
      ],
      "isManaged": true,
      "location": {},
      "nickname": "Ava Chen",
      "properties": {},
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
| `capabilitiesSupported` | array<string> | Capabilities supported by the noise sensor. |
| `connectedAccountId` | string | Connected account that owns the noise sensor. |
| `createdAt` | date | Creation timestamp. |
| `customMetadata` | object | Optional custom metadata for the noise sensor. |
| `deviceId` | string | Unique Seam device ID for the noise sensor. |
| `deviceType` | string | Noise sensor device type, such as `minut_sensor`. |
| `displayName` | string | Display name of the noise sensor. |
| `errors` | array<object> | Errors associated with the noise sensor. |
| `isManaged` | boolean | Whether the noise sensor is managed by Seam. |
| `location` | object | Location details for the noise sensor. |
| `nickname` | string | Optional noise sensor nickname. |
| `properties` | object | Noise sensor-specific properties such as battery, manufacturer, and current noise readings. |
| `warnings` | array<object> | Warnings associated with the noise sensor. |
| `workspaceId` | string | Workspace that contains the noise sensor. |

## Native endpoint

Through the native Seam API, this operation is `POST /noise_sensors/list` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-noise-sensors.md) for the provider-specific parameters and requirements.

