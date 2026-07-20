# Intervals.icu: Download Activity File

Downloads an activity file from Intervals.icu.

```
GET https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/download-activity-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intervals.icu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/download-activity-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/download-activity-file?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Intervals.icu API returns.

## Native endpoint

Through the native Intervals.icu API, this operation is `GET /api/v1/activity/:id/file` (base URL `https://intervals.icu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-activity-file.md) for the provider-specific parameters and requirements.

