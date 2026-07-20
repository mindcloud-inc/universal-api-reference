# eTermin: Unassign Calendar Services

Removes services from a calendar in eTermin.

```
DELETE https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/unassign-calendar-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/unassign-calendar-services?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/unassign-calendar-services?${params}`, {
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
| `id` | string | yes | ID of the calendar service assignment |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eTermin API returns.

## Native endpoint

Through the native eTermin API, this operation is `DELETE /api/calendarservice` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unassign-calendar-services.md) for the provider-specific parameters and requirements.

