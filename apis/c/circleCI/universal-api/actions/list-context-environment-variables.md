# CircleCI: List Context Environment Variables



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-context-environment-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-context-environment-variables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-context-environment-variables?${params}`, {
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
| `context_id` | string | no | The CircleCI context UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contextId": "string",
      "createdAt": "string",
      "updatedAt": "string",
      "variable": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contextId` | string |  |
| `createdAt` | string |  |
| `updatedAt` | string |  |
| `variable` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /context/:context_id/environment-variable` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-context-environment-variables.md) for the provider-specific parameters and requirements.

