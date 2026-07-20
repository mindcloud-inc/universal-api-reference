# Beebole: List Time Entries

Retrieves time entries from your Beebole account.

```
GET https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-time-entries?connectionId=$CONNECTION_ID&person.id=2&from=2026-03-01&to=2026-03-31" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "person.id": "2",
  "from": "2026-03-01",
  "to": "2026-03-31"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beebole/latest/actions/list-time-entries?${params}`, {
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
| `person.id` | number | yes | The Beebole person identifier whose time entries should be listed. Example: `2`. |
| `from` | string | yes | The start date for the listing window in YYYY-MM-DD format. Example: `2026-03-01`. |
| `to` | string | yes | The end date for the listing window in YYYY-MM-DD format. Example: `2026-03-31`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

