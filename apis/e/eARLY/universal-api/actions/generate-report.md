# EARLY: Generate Report

Generates a report in EARLY.

```
GET https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/generate-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/generate-report?connectionId=$CONNECTION_ID&date.start=string&date.end=string&fileType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date.start": "string",
  "date.end": "string",
  "fileType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/generate-report?${params}`, {
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
| `date.start` | string | yes | Report start date in YYYY-MM-DD format. |
| `date.end` | string | yes | Report end date in YYYY-MM-DD format. |
| `fileType` | string | yes | Report file type, for example json. |
| `operator` | string | no | Filter operator, for example OR. |
| `noteQuery` | string | no | Optional note text filter. |
| `activities.ids` | list<string> | no | Optional activity ID list. |
| `activities.status` | string | no | Optional activity status filter. |
| `users.ids` | list<string> | no | Optional user ID list. |
| `folders.ids` | list<string> | no | Optional folder ID list. |
| `tags.ids` | list<number> | no | Optional tag ID list. |
| `mentions.ids` | list<number> | no | Optional mention ID list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `POST /api/v4/report` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-report.md) for the provider-specific parameters and requirements.

