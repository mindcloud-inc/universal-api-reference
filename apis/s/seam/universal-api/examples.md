# Seam Universal API Examples

These examples use the MindCloud API key and Seam connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workspace

Retrieves the current workspace from Seam.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-workspace?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "connectPartnerName": "Ava Chen",
      "connectWebviewCustomization": {},
      "isPublishableKeyAuthEnabled": true,
      "isSandbox": true,
      "isSuspended": true,
      "name": "Ava Chen",
      "publishableKey": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Workspace action reference](actions/get-workspace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seam/latest/actions/get-workspace).

## Create Connect Webview

Creates a new connect webview in Seam.

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

Example response:

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

See the full [Create Connect Webview action reference](actions/create-connect-webview.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/seam/latest/actions/create-connect-webview).
