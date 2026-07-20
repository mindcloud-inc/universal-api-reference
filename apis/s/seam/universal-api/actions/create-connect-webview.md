# Seam: Create Connect Webview

Creates a new connect webview in Seam.

```
POST https://connect.mindcloud.co/v1/universal/seam/latest/actions/create-connect-webview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seam/latest/actions/create-connect-webview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seam/latest/actions/create-connect-webview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `providerCategory` | string | no | Provider category to show in the Connect Webview. Use `stable` for the broad sandbox-friendly path. |
| `automaticallyManageNewDevices` | boolean | no | Whether newly connected devices should be managed automatically. Seam defaults this to `true`. |
| `waitForDeviceCreation` | boolean | no | Whether the Connect Webview should wait for the first device sync before finishing. Seam defaults this to `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedCapabilities": [
        "string"
      ],
      "acceptedDevices": [
        "string"
      ],
      "acceptedProviders": [
        "string"
      ],
      "anyDeviceAllowed": true,
      "anyProviderAllowed": true,
      "authorizedAt": "2026-05-07T12:00:00.000Z",
      "automaticallyManageNewDevices": true,
      "connectedAccountId": "string",
      "connectWebviewId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customMetadata": {},
      "customRedirectFailureUrl": "https://example.com",
      "customRedirectUrl": "https://example.com",
      "deviceSelectionMode": "string",
      "loginSuccessful": true,
      "selectedProvider": "string",
      "status": "string",
      "url": "https://example.com",
      "waitForDeviceCreation": true,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedCapabilities` | array<string> | Capability filters accepted by the webview. |
| `acceptedDevices` | array<string> | Device IDs explicitly accepted by the webview. |
| `acceptedProviders` | array<string> | Provider keys accepted by the webview. |
| `anyDeviceAllowed` | boolean | Whether any device can be selected. |
| `anyProviderAllowed` | boolean | Whether any provider can be selected. |
| `authorizedAt` | date | Authorization timestamp when available. |
| `automaticallyManageNewDevices` | boolean | Whether newly connected devices are automatically managed. |
| `connectedAccountId` | string | Connected account ID after successful authorization. |
| `connectWebviewId` | string | Unique Connect Webview ID. |
| `createdAt` | date | Creation timestamp. |
| `customMetadata` | object | Custom metadata attached to the webview. |
| `customRedirectFailureUrl` | string | Custom failure redirect URL when configured. |
| `customRedirectUrl` | string | Custom success redirect URL when configured. |
| `deviceSelectionMode` | string | Device selection mode for the webview. |
| `loginSuccessful` | boolean | Whether the authorization flow completed successfully. |
| `selectedProvider` | string | Provider selected during authorization when available. |
| `status` | string | Current status of the Connect Webview. |
| `url` | string | Hosted Connect Webview URL. |
| `waitForDeviceCreation` | boolean | Whether the flow waits for device creation before finishing. |
| `workspaceId` | string | Workspace ID that owns the Connect Webview. |

## Native endpoint

Through the native Seam API, this operation is `POST /connect_webviews/create` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-connect-webview.md) for the provider-specific parameters and requirements.

