# Datarobot: Get Deployment

Retrieves details for a deployment from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-deployment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-deployment?connectionId=$CONNECTION_ID&deploymentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "deploymentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-deployment?${params}`, {
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
      "approvalStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hasError": true,
      "id": "string",
      "importance": "string",
      "label": "string",
      "status": "string",
      "userProvidedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalStatus` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `hasError` | boolean |  |
| `id` | string |  |
| `importance` | string |  |
| `label` | string |  |
| `status` | string |  |
| `userProvidedId` | string |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /deployments/:deploymentId/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deployment.md) for the provider-specific parameters and requirements.

