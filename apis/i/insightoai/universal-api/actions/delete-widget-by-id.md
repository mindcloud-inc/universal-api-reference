# Insighto.ai: Delete Widget By Id



```
DELETE https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/delete-widget-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/delete-widget-by-id?connectionId=$CONNECTION_ID&widgetId=3c90c3cc-0d44-4b50-8888-8dd25736052a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "widgetId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/delete-widget-by-id?${params}`, {
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
| `widgetId` | string | yes | The UUID id of the widget. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Insighto.ai API returns.

## Native endpoint

Through the native Insighto.ai API, this operation is `DELETE /widget/:widget_id` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-widget-by-id.md) for the provider-specific parameters and requirements.

