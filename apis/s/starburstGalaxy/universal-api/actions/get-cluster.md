# Starburst Galaxy: Get cluster



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-cluster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-cluster?connectionId=$CONNECTION_ID&clusterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clusterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-cluster?${params}`, {
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
| `clusterId` | string | yes | Starburst Galaxy cluster ID. Docs also support URL-encoded lookup expressions such as name=value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extended` | boolean | no | Whether to include extended cluster details when supported by Starburst Galaxy. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cloudRegionId": "string",
      "clusterId": "string",
      "clusterState": "string",
      "name": "Ava Chen",
      "trinoUri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cloudRegionId` | string | Cloud region ID. |
| `clusterId` | string | Cluster ID. |
| `clusterState` | string | Cluster state. |
| `name` | string | Cluster name. |
| `trinoUri` | string | Trino connection URL. |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/cluster/{clusterId}` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cluster.md) for the provider-specific parameters and requirements.

