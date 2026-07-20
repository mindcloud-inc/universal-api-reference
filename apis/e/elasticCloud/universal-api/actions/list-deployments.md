# Elastic Cloud: List Deployments

Retrieves deployments from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-deployments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-deployments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "deployments": [
        {
          "id": "string",
          "metadata": {
            "hidden": true,
            "organizationId": "string",
            "systemOwned": true
          },
          "name": "Ava Chen",
          "resources": [
            {
              "cloudId": "string",
              "elasticsearchClusterRefId": "string",
              "id": "string",
              "kind": "string",
              "refId": "string",
              "region": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deployments[].id` | string |  |
| `deployments[].metadata.hidden` | boolean |  |
| `deployments[].metadata.organizationId` | string |  |
| `deployments[].metadata.systemOwned` | boolean |  |
| `deployments[].name` | string |  |
| `deployments[].resources[].cloudId` | string |  |
| `deployments[].resources[].elasticsearchClusterRefId` | string |  |
| `deployments[].resources[].id` | string |  |
| `deployments[].resources[].kind` | string |  |
| `deployments[].resources[].refId` | string |  |
| `deployments[].resources[].region` | string |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deployments.md) for the provider-specific parameters and requirements.

