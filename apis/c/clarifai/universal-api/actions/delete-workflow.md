# Clarifai: Delete Workflow

Deletes an existing workflow from Clarifai.

```
DELETE https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/delete-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/delete-workflow?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/delete-workflow?${params}`, {
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
| `appId` | string | no | Clarifai app ID. |
| `workflowId` | string | no | Clarifai workflow ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": {
        "code": 1,
        "description": "string",
        "httpStatusCode": 1,
        "reqId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.httpStatusCode` | number |  |
| `status.reqId` | string |  |

## Native endpoint

Through the native Clarifai API, this operation is `DELETE /v2/users/{{credentials.userId}}/apps/{{appId}}/workflows/{{workflowId}}` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workflow.md) for the provider-specific parameters and requirements.

