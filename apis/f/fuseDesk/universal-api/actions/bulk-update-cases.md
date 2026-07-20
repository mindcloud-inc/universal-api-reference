# FuseDesk: Bulk Update Cases

Updates multiple existing cases in FuseDesk.

```
PUT https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/bulk-update-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/bulk-update-cases" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "caseIds": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/bulk-update-cases', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "caseIds": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `caseIds` | string | yes |  |
| `crmAutomationId` | number | no |  |
| `crmTagId` | number | no |  |
| `departmentId` | number | no |  |
| `merge` | boolean | no |  |
| `repId` | number | no |  |
| `snooze` | string | no |  |
| `status` | string | no |  |
| `tagId` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `POST /api/v1/cases/update` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-cases.md) for the provider-specific parameters and requirements.

