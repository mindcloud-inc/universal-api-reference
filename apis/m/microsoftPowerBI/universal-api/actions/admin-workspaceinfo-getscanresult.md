# Microsoft Power BI: WorkspaceInfo GetScanResult



```
GET https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-getscanresult
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-getscanresult?connectionId=$CONNECTION_ID&scanId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scanId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/admin-workspaceinfo-getscanresult?${params}`, {
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
| `scanId` | string | yes | The scan ID, which is included in the response from the workspaces or the Admin - WorkspaceInfo PostWorkspaceInfo API call that triggered the scan. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `GET admin/workspaces/scanResult/[:scanId]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/admin-workspaceinfo-getscanresult.md) for the provider-specific parameters and requirements.

