# Markup AI: Get Style Check

Retrieves style check results from Markup AI.

```
GET https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-style-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-style-check?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-style-check?${params}`, {
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
| `workflowId` | string | yes | Workflow ID for the style check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "original": {},
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `original` | object |  |
| `workflow` | object |  |

## Native endpoint

Through the native Markup AI API, this operation is `GET /v1/style/checks/:workflow_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-style-check.md) for the provider-specific parameters and requirements.

