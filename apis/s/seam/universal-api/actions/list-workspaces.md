# Seam: List Workspaces

Retrieves a list of workspaces from Seam.

```
GET https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seam/latest/actions/list-workspaces?${params}`, {
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
| `companyName` | string |  |
| `connectPartnerName` | string |  |
| `connectWebviewCustomization` | object |  |
| `isPublishableKeyAuthEnabled` | boolean |  |
| `isSandbox` | boolean |  |
| `isSuspended` | boolean |  |
| `name` | string |  |
| `publishableKey` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Seam API, this operation is `POST /workspaces/list` (base URL `https://connect.getseam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

