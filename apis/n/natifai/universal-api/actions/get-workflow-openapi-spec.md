# Natif.ai: Get Workflow OpenAPI Spec

Retrieves the OpenAPI spec for a Natif.ai workflow.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-workflow-openapi-spec
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-workflow-openapi-spec?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/get-workflow-openapi-spec?${params}`, {
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
| `workflowId` | string | yes | Workflow identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": {},
      "info": {},
      "openapi": "string",
      "paths": {},
      "security": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | object |  |
| `info` | object |  |
| `openapi` | string |  |
| `paths` | object |  |
| `security` | array<object> |  |

## Native endpoint

Through the native Natif.ai API, this operation is `GET /processing/[:workflowId]/openapi` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-openapi-spec.md) for the provider-specific parameters and requirements.

