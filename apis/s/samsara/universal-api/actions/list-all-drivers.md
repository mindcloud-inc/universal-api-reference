# Samsara: List Drivers



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-all-drivers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-all-drivers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-all-drivers?${params}`, {
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
| `driverActivationStatus` | string | no | Filter drivers by active or deactivated status. |
| `createdAfterTime` | string | no | Return drivers created at or after this RFC 3339 timestamp. |
| `updatedAfterTime` | string | no | Return drivers updated at or after this RFC 3339 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrierSettings": {
        "carrierName": "Ava Chen",
        "dotNumber": 1,
        "homeTerminalAddress": "string",
        "homeTerminalName": "Ava Chen",
        "mainOfficeAddress": "string"
      },
      "createdAtTime": "string",
      "driverActivationStatus": "string",
      "eldExempt": true,
      "eldExemptReason": "string",
      "hasVehicleUnpinningEnabled": true,
      "hosSetting": {
        "heavyHaulExemptionToggleEnabled": true
      },
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "tags": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "timezone": "string",
      "updatedAtTime": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrierSettings.carrierName` | string |  |
| `carrierSettings.dotNumber` | number |  |
| `carrierSettings.homeTerminalAddress` | string |  |
| `carrierSettings.homeTerminalName` | string |  |
| `carrierSettings.mainOfficeAddress` | string |  |
| `createdAtTime` | string |  |
| `driverActivationStatus` | string |  |
| `eldExempt` | boolean |  |
| `eldExemptReason` | string |  |
| `hasVehicleUnpinningEnabled` | boolean |  |
| `hosSetting.heavyHaulExemptionToggleEnabled` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `tags[].id` | string |  |
| `tags[].name` | string |  |
| `timezone` | string |  |
| `updatedAtTime` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Samsara API, this operation is `GET fleet/drivers` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-drivers.md) for the provider-specific parameters and requirements.

