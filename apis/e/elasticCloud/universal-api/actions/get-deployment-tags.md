# Elastic Cloud: Get Deployment Tags

Retrieves deployment tags from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-tags?connectionId=$CONNECTION_ID&deploymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-tags?${params}`, {
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
| `deploymentId` | string | yes | Identifier for the deployment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        {
          "key": "string",
          "value": "string"
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
| `tags[].key` | string |  |
| `tags[].value` | string |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments/:deployment_id/tags` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment-tags.md) for the provider-specific parameters and requirements.

