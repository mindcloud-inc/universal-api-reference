# WaniKani: List Spaced Repetition Systems

Retrieves spaced repetition systems from WaniKani.

```
GET https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-spaced-repetition-systems
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-spaced-repetition-systems?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-spaced-repetition-systems?${params}`, {
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
| `ids` | string | no | Filter spaced repetition systems by a comma-separated list of IDs. Example: `1,2`. |
| `updatedAfter` | date | no | Return spaced repetition systems updated after this ISO 8601 timestamp. Example: `2026-01-01T00:00:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaniKani API returns.

## Native endpoint

Through the native WaniKani API, this operation is `GET /spaced_repetition_systems` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-spaced-repetition-systems.md) for the provider-specific parameters and requirements.

