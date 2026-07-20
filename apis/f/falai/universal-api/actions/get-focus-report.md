# fal.ai: Get FOCUS Report

Retrieves a FOCUS billing report from fal.ai.

```
GET https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-focus-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fal.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-focus-report?connectionId=$CONNECTION_ID&source=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/falai/latest/actions/get-focus-report?${params}`, {
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
| `source` | string | yes | FOCUS report source value required by fal.ai. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native fal.ai API returns.

## Native endpoint

Through the native fal.ai API, this operation is `GET /account/focus` (base URL `https://api.fal.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-focus-report.md) for the provider-specific parameters and requirements.

