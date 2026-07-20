# Beebole: Get a Time Entry

Retrieves a time entry from your Beebole account.

```
GET https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-a-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-a-time-entry?connectionId=$CONNECTION_ID&id=1&date=2026-03-23" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "date": "2026-03-23"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beebole/latest/actions/get-a-time-entry?${params}`, {
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
| `id` | number | yes | The Beebole time entry identifier. |
| `date` | string | yes | The time entry date in YYYY-MM-DD format. Example: `2026-03-23`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-time-entry.md) for the provider-specific parameters and requirements.

