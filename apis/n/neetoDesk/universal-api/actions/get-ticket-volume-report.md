# NeetoDesk: Get Ticket Volume Report



```
GET https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/get-ticket-volume-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/get-ticket-volume-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoDesk/latest/actions/get-ticket-volume-report?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rangeType` | string | no | Date range preset for the report. |
| `startDate` | date | no | Start date for a custom range. |
| `endDate` | date | no | End date for a custom range. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoDesk API returns.

## Native endpoint

Through the native NeetoDesk API, this operation is `GET /reports/tickets` (base URL `https://{{credentials.workspaceSubdomain}}.neetodesk.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-volume-report.md) for the provider-specific parameters and requirements.

