# Seam: List Thermostats

Retrieves a list of thermostats from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-thermostats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-thermostats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-thermostats?${params}`, {
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
| `connectedAccountId` | string | no | ID of the connected account for which you want to list thermostats. |
| `search` | string | no | Search string for thermostats. |
| `spaceId` | string | no | ID of the space for which you want to list thermostats. |

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

Through the native Seam API, this operation is `POST /thermostats/list` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-thermostats.md) for the provider-specific parameters and requirements.

