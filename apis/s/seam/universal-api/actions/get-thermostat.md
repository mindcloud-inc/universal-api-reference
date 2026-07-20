# Seam: Get Thermostat



```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-thermostat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-thermostat?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-thermostat?${params}`, {
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
| `deviceId` | string | no | ID of the thermostat device that you want to get. |
| `name` | string | no | Name of the thermostat device that you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canHvacCool": true,
      "canHvacHeat": true,
      "canHvacHeatCool": true,
      "canTurnOffHvac": true,
      "connectedAccountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
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
| `canHvacCool` | boolean | Whether cooling is supported. |
| `canHvacHeat` | boolean | Whether heating is supported. |
| `canHvacHeatCool` | boolean | Whether heat-cool mode is supported. |
| `canTurnOffHvac` | boolean | Whether HVAC can be turned off. |
| `connectedAccountId` | string | Connected account that owns the thermostat. |
| `createdAt` | date | Creation timestamp. |
| `deviceId` | string | Unique Seam device ID for the thermostat. |
| `deviceManufacturer` | object | Manufacturer information for the thermostat. |
| `deviceProvider` | object | Provider information for the thermostat. |
| `deviceType` | string | Thermostat device type. |
| `displayName` | string | Display name of the thermostat. |
| `errors` | array<object> | Errors associated with the thermostat. |
| `isManaged` | boolean | Whether the thermostat is managed by Seam. |
| `location` | object | Location details for the thermostat. |
| `nickname` | string | Optional thermostat nickname. |
| `warnings` | array<object> | Warnings associated with the thermostat. |
| `workspaceId` | string | Workspace that contains the thermostat. |

## Native endpoint

Through the native Seam API, this operation is `POST /thermostats/get` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thermostat.md) for the provider-specific parameters and requirements.

