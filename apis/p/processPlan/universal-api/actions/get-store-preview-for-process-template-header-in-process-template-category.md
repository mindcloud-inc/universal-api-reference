# Process Plan: Get Store Preview for Process Template Header in Process Template Category



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-store-preview-for-process-template-header-in-process-template-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-store-preview-for-process-template-header-in-process-template-category?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-store-preview-for-process-template-header-in-process-template-category?${params}`, {
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
| `processTemplateCategoryId` | string | no | Process template category ID. |
| `processTemplateHeaderId` | string | no | Process template header ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Plan API returns.

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_category/:processTemplateCategoryId/process_template_header/:processTemplateHeaderId/store_preview` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-store-preview-for-process-template-header-in-process-template-category.md) for the provider-specific parameters and requirements.

