# SEOTakeoff: List Clusters



```
GET https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-clusters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-clusters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-clusters?${params}`, {
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
| `since` | date | no | Only return clusters created after this ISO timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "keyword_count": 1,
      "name": "Ava Chen",
      "website_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the cluster was created. |
| `id` | string | Unique cluster ID. |
| `keyword_count` | number | Number of keywords in the cluster. |
| `name` | string | Cluster name. |
| `website_id` | string | Website ID that owns the cluster. |

## Native endpoint

Through the native SEOTakeoff API, this operation is `GET /api/zapier/clusters` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clusters.md) for the provider-specific parameters and requirements.

