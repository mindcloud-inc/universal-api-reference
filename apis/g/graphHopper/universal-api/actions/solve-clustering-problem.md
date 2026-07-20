# GraphHopper: Solve Clustering Problem

Solves a clustering problem in GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/solve-clustering-problem
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/solve-clustering-problem?connectionId=$CONNECTION_ID&requestBody=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestBody": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/solve-clustering-problem?${params}`, {
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
| `requestBody` | object | yes | Clustering request JSON body matching GraphHopper's ClusterRequest schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clusters": [
        {}
      ],
      "copyrights": [
        "string"
      ],
      "processing_time": 1,
      "status": "string",
      "waiting_time_in_queue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clusters` | array<object> | Cluster results. |
| `copyrights` | array<string> | Attribution strings. |
| `processing_time` | number | Processing time. |
| `status` | string | Clustering status. |
| `waiting_time_in_queue` | number | Queue wait time. |

## Native endpoint

Through the native GraphHopper API, this operation is `POST /cluster` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/solve-clustering-problem.md) for the provider-specific parameters and requirements.

