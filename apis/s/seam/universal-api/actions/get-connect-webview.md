# Seam: Get Connect Webview

Retrieves a connect webview from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-connect-webview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-connect-webview?connectionId=$CONNECTION_ID&connectWebviewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectWebviewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-connect-webview?${params}`, {
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
| `connectWebviewId` | string | yes |  |

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
| `acceptedCapabilities` | array<string> |  |
| `acceptedDevices` | array<string> |  |
| `acceptedProviders` | array<string> |  |
| `anyDeviceAllowed` | boolean |  |
| `anyProviderAllowed` | boolean |  |
| `authorizedAt` | date |  |
| `automaticallyManageNewDevices` | boolean |  |
| `connectedAccountId` | string |  |
| `connectWebviewId` | string |  |
| `createdAt` | date |  |
| `customMetadata` | object |  |
| `customRedirectFailureUrl` | string |  |
| `customRedirectUrl` | string |  |
| `deviceSelectionMode` | string |  |
| `loginSuccessful` | boolean |  |
| `selectedProvider` | string |  |
| `status` | string |  |
| `url` | string |  |
| `waitForDeviceCreation` | boolean |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Seam API, this operation is `POST /connect_webviews/get` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connect-webview.md) for the provider-specific parameters and requirements.

