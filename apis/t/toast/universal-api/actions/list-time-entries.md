# Toast: List Time Entries

Retrieves employee time entries using identifiers, date ranges, modification ranges, or business date.

```
GET https://connect.mindcloud.co/v1/universal/toast/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toast/latest/actions/list-time-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toast/latest/actions/list-time-entries?${params}`, {
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
| `timeEntryIds` | string | no | One or more Toast GUIDs or external time-entry identifiers, with a maximum of 100. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | date | no | Inclusive clock-in beginning of the time-entry range in ISO-8601 format. Example: `2026-07-01T00:00:00Z`. |
| `endDate` | date | no | Exclusive clock-in end of the time-entry range in ISO-8601 format. Example: `2026-07-31T23:59:59Z`. |
| `modifiedStartDate` | date | no | Inclusive beginning of the modification range in ISO-8601 format. Example: `2026-07-01T00:00:00Z`. |
| `modifiedEndDate` | date | no | Exclusive end of the modification range in ISO-8601 format. Example: `2026-07-31T23:59:59Z`. |
| `businessDate` | date | no | Restaurant business date in yyyyMMdd format. Example: `20260731`. |
| `includeMissedBreaks` | boolean | no | Include missed breaks in each time entry break array. |
| `includeArchived` | boolean | no | Include archived time entries when selecting by start and end date. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Toast API returns.

## Native endpoint

Through the native Toast API, this operation is `GET /labor/v1/timeEntries` (base URL `{{credentials.connection}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

