# Memix: Get Template Details

Retrieves full template details from Memix.

```
GET https://connect.mindcloud.co/v1/universal/memix/latest/actions/get-template-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memix/latest/actions/get-template-details?connectionId=$CONNECTION_ID&template_slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memix/latest/actions/get-template-details?${params}`, {
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
| `template_slug` | string | yes | Memix template slug. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Memix API returns.

## Native endpoint

Through the native Memix API, this operation is `GET /v1/templates/:template_slug` (base URL `https://api.memix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-details.md) for the provider-specific parameters and requirements.

