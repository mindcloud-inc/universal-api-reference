# WaniKani: Get Spaced Repetition System

Retrieves a spaced repetition system from WaniKani.

```
GET https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-spaced-repetition-system
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-spaced-repetition-system?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-spaced-repetition-system?${params}`, {
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
| `id` | number | yes | The spaced repetition system ID to retrieve. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaniKani API returns.

## Native endpoint

Through the native WaniKani API, this operation is `GET /spaced_repetition_systems/:id` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spaced-repetition-system.md) for the provider-specific parameters and requirements.

