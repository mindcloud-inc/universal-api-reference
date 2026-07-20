# Walla Form: Get Response by Response Key



```
GET https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-response-by-response-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walla Form `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-response-by-response-key?connectionId=$CONNECTION_ID&workspaceKey=string&projectKey=string&responseKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceKey": "string",
  "projectKey": "string",
  "responseKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-response-by-response-key?${params}`, {
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
| `workspaceKey` | string | yes | The Walla workspace key. |
| `projectKey` | string | yes | The Walla project key. |
| `responseKey` | string | yes | The response key returned by Walla. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object |  |

## Native endpoint

Through the native Walla Form API, this operation is `GET /workspace/:workspaceKey/project/:projectKey/response/get/responseKey/:responseKey` (base URL `https://walla-api.data-lab.workers.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response-by-response-key.md) for the provider-specific parameters and requirements.

