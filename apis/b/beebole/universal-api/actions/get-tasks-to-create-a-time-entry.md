# Beebole: Get Tasks to Create a Time Entry

Retrieves tasks for creating a time entry in Beebole.

```
GET https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-tasks-to-create-a-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-tasks-to-create-a-time-entry?connectionId=$CONNECTION_ID&subproject.id=37&date=2026-03-23" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subproject.id": "37",
  "date": "2026-03-23"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-tasks-to-create-a-time-entry?${params}`, {
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
| `subproject.id` | number | yes | The Beebole subproject identifier whose available tasks should be listed. Example: `37`. |
| `project.id` | number | no | Optional project identifier used when tasks are configured directly on a project in the connected account. Example: `26`. |
| `date` | string | yes | The date used by Beebole to evaluate which tasks are available. Example: `2026-03-23`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tasks-to-create-a-time-entry.md) for the provider-specific parameters and requirements.

