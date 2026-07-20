# FuseDesk: Archive Department

Archives an existing department in FuseDesk.

```
DELETE https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/archive-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/archive-department?connectionId=$CONNECTION_ID&departmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "departmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/archive-department?${params}`, {
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
| `departmentId` | number | yes | The FuseDesk department ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `DELETE /api/v2/departments/:departmentId` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-department.md) for the provider-specific parameters and requirements.

