# Process Plan: Store Purchase for Process Template Header for Process Template Category



```
POST https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/store-purchase-for-process-template-header-for-process-template-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/store-purchase-for-process-template-header-for-process-template-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/store-purchase-for-process-template-header-for-process-template-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processTemplateCategoryId` | string | no | Process template category ID. |
| `processTemplateHeaderId` | string | no | Process template header ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Plan API returns.

## Native endpoint

Through the native Process Plan API, this operation is `POST /process_template_category/:processTemplateCategoryId/process_template_header/:processTemplateHeaderId/store_purchase` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-purchase-for-process-template-header-for-process-template-category.md) for the provider-specific parameters and requirements.

