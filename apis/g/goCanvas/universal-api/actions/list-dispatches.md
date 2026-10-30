# GoCanvas: List Dispatches



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-dispatches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-dispatches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-dispatches?${params}`, {
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
| `userId` | number | no | Assigned user ID. Provide at least one of User ID, Department ID, or Form ID. |
| `departmentId` | number | no | Department ID. Provide at least one of User ID, Department ID, or Form ID. |
| `formId` | number | no | Form ID. Provide at least one of User ID, Department ID, or Form ID. |
| `projectId` | number | no | Restrict results to dispatches assigned to this project. |
| `status` | list | no | Ready ignores date filters and returns eligible assigned or received dispatches for the requested/current user. One of: `assigned`, `ready`, `received`, `unassigned`. |
| `startDate` | string | no | Beginning bound for created_at, in ISO 8601. |
| `endDate` | string | no | Ending bound for created_at, in ISO 8601. |
| `scheduledStartDate` | string | no | Beginning bound for scheduled_at, in ISO 8601. |
| `scheduledEndDate` | string | no | Ending bound for scheduled_end, in ISO 8601. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `GET /dispatches` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dispatches.md) for the provider-specific parameters and requirements.

