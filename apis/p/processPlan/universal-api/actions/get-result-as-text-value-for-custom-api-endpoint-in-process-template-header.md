# Process Plan: Get Result As Text Value for Custom API Endpoint in Process Template Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-result-as-text-value-for-custom-api-endpoint-in-process-template-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-result-as-text-value-for-custom-api-endpoint-in-process-template-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-result-as-text-value-for-custom-api-endpoint-in-process-template-header?${params}`, {
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
| `customAPIEndpointId` | string | no | Custom API endpoint ID. |
| `processTemplateHeaderId` | string | no | Process template header ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Plan API returns.

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/:processTemplateHeaderId/custom_api_endpoint/:customAPIEndpointId/result/as_text_value` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-result-as-text-value-for-custom-api-endpoint-in-process-template-header.md) for the provider-specific parameters and requirements.

