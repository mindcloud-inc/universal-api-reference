# WaniKani: Get Level Progression

Retrieves a level progression from WaniKani.

```
GET https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-level-progression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-level-progression?connectionId=$CONNECTION_ID&id=4124952" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "4124952"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-level-progression?${params}`, {
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
| `id` | number | yes | The level progression ID to retrieve. Example: `4124952`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaniKani API returns.

## Native endpoint

Through the native WaniKani API, this operation is `GET /level_progressions/:id` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-level-progression.md) for the provider-specific parameters and requirements.

