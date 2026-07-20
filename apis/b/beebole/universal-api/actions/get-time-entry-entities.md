# Beebole: Get Time Entry Entities

Retrieves available entities for a time entry in Beebole.

```
GET https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-time-entry-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-time-entry-entities?connectionId=$CONNECTION_ID&date=2026-03-23" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-03-23"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-time-entry-entities?${params}`, {
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
| `company.id` | number | no | Provide a Beebole company ID to list its available projects for time entry creation. Example: `3`. |
| `project.id` | number | no | Provide a Beebole project ID to list its available subprojects for time entry creation. Example: `30`. |
| `date` | string | yes | The date used by Beebole to evaluate which entities are available. Example: `2026-03-23`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry-entities.md) for the provider-specific parameters and requirements.

