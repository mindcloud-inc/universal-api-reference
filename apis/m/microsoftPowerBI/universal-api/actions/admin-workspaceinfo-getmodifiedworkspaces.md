# Microsoft Power BI: WorkspaceInfo GetModifiedWorkspaces



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-getmodifiedworkspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-getmodifiedworkspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-getmodifiedworkspaces?${params}`, {
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
| `excludeInActiveWorkspaces` | boolean | no | Whether to exclude inactive workspaces |
| `excludePersonalWorkspaces` | boolean | no | Whether to exclude personal workspaces |
| `modifiedSince` | date | no | Last modified date (must be in ISO 8601 compliant UTC format) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET admin/workspaces/modified` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-workspaceinfo-getmodifiedworkspaces.md) for the provider-specific parameters and requirements.

