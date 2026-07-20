# SEOTakeoff: Research Keywords



```
POST https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/research-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/research-keywords" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clusterId": "string",
  "seedTopic": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/research-keywords', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clusterId": "string",
    "seedTopic": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clusterId` | string | yes | Cluster ID to research. |
| `seedTopic` | string | yes | Topic to research for new keywords. |
| `count` | number | no | Number of keywords to research, between 5 and 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cluster_id": "string",
      "cluster_name": "Ava Chen",
      "keywords_requested": 1,
      "message": "string",
      "status": "string",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cluster_id` | string |  |
| `cluster_name` | string |  |
| `keywords_requested` | number |  |
| `message` | string |  |
| `status` | string |  |
| `topic` | string |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `POST /api/zapier/clusters/research-keywords` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/research-keywords.md) for the provider-specific parameters and requirements.

