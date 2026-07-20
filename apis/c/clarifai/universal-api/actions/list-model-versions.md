# Clarifai: List Model Versions

Retrieves model versions from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-model-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-model-versions?connectionId=$CONNECTION_ID&limit=25&offset=0&appId=string&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "appId": "string",
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-model-versions?${params}`, {
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
| `appId` | string | yes | Clarifai app ID. |
| `modelId` | string | yes | Clarifai model ID. |
| `trainedOnly` | boolean | no | Return only trained versions. |
| `conceptIds` | string | no | Filter by concept IDs. |

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

Through the native Clarifai API, this operation is `GET /v2/users/me/apps/:appId/models/:modelId/versions` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-model-versions.md) for the provider-specific parameters and requirements.

