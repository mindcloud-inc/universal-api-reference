# Cerebras AI: Retrieve Model Version Status

Retrieves model version status from Cerebras AI.

```
GET https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-model-version-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerebras AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-model-version-status?connectionId=$CONNECTION_ID&orgName=Ava%20Chen&modelArchId=string&versionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgName": "Ava Chen",
  "modelArchId": "string",
  "versionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerebrasAI/latest/actions/retrieve-model-version-status?${params}`, {
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
| `orgName` | string | yes |  |
| `modelArchId` | string | yes |  |
| `versionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean |  |
| `name` | string |  |
| `response` | object |  |

## Native endpoint

Through the native Cerebras AI API, this operation is `GET /management/v1/orgs/:orgName/models/:modelArchId/versions/:versionId` (base URL `https://api.cerebras.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-model-version-status.md) for the provider-specific parameters and requirements.

