# Beehiiv: Get Publication Post Aggregate Stats

Retrieves aggregate stats for publication posts from Beehiiv.

```
GET https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-post-aggregate-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beehiiv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-post-aggregate-stats?connectionId=$CONNECTION_ID&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/get-publication-post-aggregate-stats?${params}`, {
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
| `publicationId` | string | yes | The prefixed ID of the publication object. |
| `audience` | string | no | Optionally filter the results by audience. |
| `platform` | string | no | Optionally filter the results by platform. |
| `status` | string | no | Optionally filter the results by post status. |
| `contentTags[]` | array<string> | no | Optionally filter posts by content tags. |
| `authors[]` | array<string> | no | Optionally filter posts by author names. |
| `hiddenFromFeed` | string | no | Optionally filter by hidden_from_feed state. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beehiiv API returns.

## Native endpoint

Through the native Beehiiv API, this operation is `GET /v2/publications/:publicationId/posts/aggregate_stats` (base URL `https://api.beehiiv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-publication-post-aggregate-stats.md) for the provider-specific parameters and requirements.

