# Kadoa: Create Workflow



```
POST https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls": "https://example.com",
  "entity": "e.g. Product, Job",
  "fields": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls": "https://example.com",
    "entity": "e.g. Product, Job",
    "fields": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urls` | list<string> | yes | JSON array of URLs to extract from Example: `https://example.com`. |
| `entity` | string | yes | Entity type to extract Example: `e.g. Product, Job`. |
| `fields` | list<object> | yes | JSON array of field definitions Example: `[object Object]`. |
| `name` | string | no | Workflow name |
| `description` | string | no | Workflow description |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `navigationMode` | string | no | Navigation mode: single-page, paginated-page, page-and-detail, agentic-navigation, all-pages |
| `maxItems` | number | no | Max items to extract |
| `maxPages` | number | no | Max pages to process |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "message": "string",
      "success": true,
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Provider error detail when request fails. |
| `message` | string | Provider status message. |
| `success` | boolean | Whether workflow creation succeeded. |
| `workflowId` | string | Created workflow identifier. |

## Native endpoint

Through the native Kadoa API, this operation is `POST /v4/workflows/` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

