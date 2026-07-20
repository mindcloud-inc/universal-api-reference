# Walla Form: Get Response by Customer Key



```
GET https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-response-by-customer-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walla Form `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-response-by-customer-key?connectionId=$CONNECTION_ID&workspaceKey=string&projectKey=string&customerKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceKey": "string",
  "projectKey": "string",
  "customerKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-response-by-customer-key?${params}`, {
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
| `customerKey` | string | yes | The customer key recorded in the Walla response. |

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

Through the native Walla Form API, this operation is `GET /workspace/:workspaceKey/project/:projectKey/response/get/customerKey/:customerKey` (base URL `https://walla-api.data-lab.workers.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response-by-customer-key.md) for the provider-specific parameters and requirements.

