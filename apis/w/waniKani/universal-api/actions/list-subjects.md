# WaniKani: List Subjects

Retrieves subjects from WaniKani.

```
GET https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-subjects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-subjects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/list-subjects?${params}`, {
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
| `ids` | string | no | Comma-delimited subject IDs to include. Example: `123,456`. |
| `types` | string | no | Comma-delimited subject types to include. Example: `radical,kanji`. |
| `slugs` | string | no | Comma-delimited subject slugs to include. Example: `一,食べる`. |
| `levels` | string | no | Comma-delimited level numbers to include. Example: `1,2,3`. |
| `hidden` | boolean | no | Whether to include hidden or visible subjects. Example: `true`. |
| `updatedAfter` | date | no | Only return subjects updated after this ISO-8601 timestamp. Example: `2026-04-01T00:00:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaniKani API returns.

## Native endpoint

Through the native WaniKani API, this operation is `GET /subjects` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subjects.md) for the provider-specific parameters and requirements.

