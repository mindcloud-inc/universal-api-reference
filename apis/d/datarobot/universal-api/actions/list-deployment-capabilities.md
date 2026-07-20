# Datarobot: List Deployment Capabilities

Retrieves capabilities for a deployment from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-deployment-capabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-deployment-capabilities?connectionId=$CONNECTION_ID&deploymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-deployment-capabilities?${params}`, {
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
| `deploymentId` | string | yes | The unique identifier of the deployment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        "string"
      ],
      "name": "Ava Chen",
      "supported": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages` | array<string> |  |
| `name` | string |  |
| `supported` | boolean |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /deployments/:deploymentId/capabilities/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deployment-capabilities.md) for the provider-specific parameters and requirements.

