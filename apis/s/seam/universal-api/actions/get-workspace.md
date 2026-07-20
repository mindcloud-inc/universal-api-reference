# Seam: Get Workspace

Retrieves the current workspace from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string | Company name associated with the workspace. |
| `connectPartnerName` | string | Deprecated connect partner name. |
| `connectWebviewCustomization` | object | Workspace-level Connect Webview customization settings. |
| `isPublishableKeyAuthEnabled` | boolean | Whether publishable key auth is enabled. |
| `isSandbox` | boolean | Whether the workspace is a sandbox workspace. |
| `isSuspended` | boolean | Whether the sandbox workspace is suspended. |
| `name` | string | Workspace name. |
| `publishableKey` | string | Workspace publishable key when available. |
| `workspaceId` | string | Unique Seam workspace ID. |

## Native endpoint

Through the native Seam API, this operation is `POST /workspaces/get` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

