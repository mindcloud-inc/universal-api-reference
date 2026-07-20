# Seam: List Device Providers

Retrieves a list of device providers from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-device-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-device-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-device-providers?${params}`, {
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
| `providerCategory` | string | no | Category for which you want to list providers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canProgramOfflineAccessCodes": true,
      "canProgramOnlineAccessCodes": true,
      "canRemotelyLock": true,
      "canRemotelyUnlock": true,
      "canSimulateConnection": true,
      "canSimulateDisconnection": true,
      "canSimulateRemoval": true,
      "deviceProviderName": "Ava Chen",
      "displayName": "Ava Chen",
      "imageUrl": "https://example.com",
      "providerCategories": [
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
| `canProgramOfflineAccessCodes` | boolean |  |
| `canProgramOnlineAccessCodes` | boolean |  |
| `canRemotelyLock` | boolean |  |
| `canRemotelyUnlock` | boolean |  |
| `canSimulateConnection` | boolean |  |
| `canSimulateDisconnection` | boolean |  |
| `canSimulateRemoval` | boolean |  |
| `deviceProviderName` | string |  |
| `displayName` | string |  |
| `imageUrl` | string |  |
| `providerCategories` | array<string> |  |

## Native endpoint

Through the native Seam API, this operation is `POST /devices/list_device_providers` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-device-providers.md) for the provider-specific parameters and requirements.

