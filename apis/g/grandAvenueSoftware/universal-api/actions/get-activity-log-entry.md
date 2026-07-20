# Grand Avenue Software: Get Activity Log Entry

Retrieves an activity log entry from Grand Avenue Software by ID.

```
GET https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-activity-log-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grand Avenue Software `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-activity-log-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grandAvenueSoftware/latest/actions/get-activity-log-entry?${params}`, {
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
| `select` | list<string> | no | Accepts multiple values in one string. |
| `expand` | list<string> | no | Accepts multiple values in one string. |
| `id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Grand Avenue Software API returns.

## Native endpoint

Through the native Grand Avenue Software API, this operation is `GET /ActivityLogEntries/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity-log-entry.md) for the provider-specific parameters and requirements.

