# Zoho Analytics: Get Workspace

Retrieves a workspace from Zoho Analytics by ID.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | string | yes | ID of the workspace to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "workspaces": {
          "createdBy": "string",
          "createdTime": "string",
          "orgId": "string",
          "workspaceDesc": "string",
          "workspaceId": "string",
          "workspaceName": "Ava Chen"
        }
      },
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.workspaces.createdBy` | string |  |
| `data.workspaces.createdTime` | string |  |
| `data.workspaces.orgId` | string |  |
| `data.workspaces.workspaceDesc` | string |  |
| `data.workspaces.workspaceId` | string |  |
| `data.workspaces.workspaceName` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /workspaces/[:workspace-id]` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

