# ShortPen: List Link Click Analytics

Retrieves click analytics for one ShortPen link by date range.

```
GET https://connect.mindcloud.co/v1/universal/shortPen/latest/actions/list-link-click-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShortPen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortPen/latest/actions/list-link-click-analytics?connectionId=$CONNECTION_ID&start=string&end=string&url_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "string",
  "end": "string",
  "url_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortPen/latest/actions/list-link-click-analytics?${params}`, {
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
| `start` | string | yes | Inclusive start date in YYYY-MM-DD format. |
| `end` | string | yes | Inclusive end date in YYYY-MM-DD format. |
| `url_id` | number | yes | ShortPen link ID to filter analytics for a single link. |
| `workspace_id` | number | no | Optional workspace scope for the analytics export. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShortPen API returns.

## Native endpoint

Through the native ShortPen API, this operation is `POST /v1/analytics` (base URL `https://api.shortpen.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-link-click-analytics.md) for the provider-specific parameters and requirements.

