# Short.io: Get Link Clicks By Paths

Retrieves link clicks from Short.io by paths.

```
GET https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-clicks-by-paths
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-clicks-by-paths?connectionId=$CONNECTION_ID&domainId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortio/latest/actions/get-link-clicks-by-paths?${params}`, {
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
| `domainId` | number | yes | Domain ID. |
| `paths[]` | array<string> | no | Optional link path selector list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Short.io API returns.

## Native endpoint

Through the native Short.io API, this operation is `POST https://statistics.short.io/statistics/domain/:domainId/link_clicks` (base URL `https://api.short.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-clicks-by-paths.md) for the provider-specific parameters and requirements.

