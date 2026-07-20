# UserVitals: Get Widget Ideas

Retrieves widget ideas for a roadmap from the roadmap API.

```
GET https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-widget-ideas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-widget-ideas?connectionId=$CONNECTION_ID&roadmapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roadmapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-widget-ideas?${params}`, {
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
| `roadmapId` | string | yes | The roadmap id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `GET /roadmaps/:id/widget` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget-ideas.md) for the provider-specific parameters and requirements.

