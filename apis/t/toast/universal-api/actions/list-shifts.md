# Toast: List Shifts

Retrieves labor shifts by identifier or by an ISO-8601 date range of up to one month.

```
GET https://connect.mindcloud.co/v1/universal/toast/latest/actions/list-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toast/latest/actions/list-shifts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toast/latest/actions/list-shifts?${params}`, {
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
| `shiftIds` | string | no | One or more Toast GUIDs or external shift identifiers, with a maximum of 100. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | date | no | Inclusive beginning of the shift date range in ISO-8601 format. Example: `2026-07-01T00:00:00Z`. |
| `endDate` | date | no | Exclusive end of the shift date range in ISO-8601 format. Example: `2026-07-31T23:59:59Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Toast API returns.

## Native endpoint

Through the native Toast API, this operation is `GET /labor/v1/shifts` (base URL `{{credentials.connection}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shifts.md) for the provider-specific parameters and requirements.

