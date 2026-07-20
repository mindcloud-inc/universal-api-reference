# Cloudflare Browser Run: Get JSON

Retrieves structured JSON from Cloudflare Browser Run.

```
GET https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-json?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/get-json?${params}`, {
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
| `html` | string | no | HTML content to render. Either HTML or URL must be set. |
| `url` | string | no | URL to navigate to. Either URL or HTML must be set. |
| `prompt` | string | no | Prompt to use for JSON extraction. Pass prompt or response format fields as documented. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseFormat` | object | no | Workers AI JSON-mode response format object with type and optional json_schema. |
| `customAi[]` | array<object> | no | Optional ordered list of custom AI model configurations for JSON extraction. |
| `cacheTTL` | number | no | Cache TTL in seconds. Set 0 to disable cache. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloudflare Browser Run API returns.

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `POST /accounts/:accountId/browser-rendering/json` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-json.md) for the provider-specific parameters and requirements.

