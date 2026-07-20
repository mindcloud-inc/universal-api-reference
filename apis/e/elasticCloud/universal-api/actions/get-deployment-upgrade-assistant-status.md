# Elastic Cloud: Get Deployment Upgrade Assistant Status

Retrieves deployment upgrade assistant status from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-upgrade-assistant-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-upgrade-assistant-status?connectionId=$CONNECTION_ID&deploymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/get-deployment-upgrade-assistant-status?${params}`, {
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
| `targetVersion` | string | no | Optional target version to include in the upgrade assistant request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "readyForUpgrade": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string |  |
| `readyForUpgrade` | boolean |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments/:deployment_id/upgrade_assistant/status` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment-upgrade-assistant-status.md) for the provider-specific parameters and requirements.

