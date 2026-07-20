# Grok: Delete Previous Response

Deletes a previous response from Grok.

```
DELETE https://connect.mindcloud.co/v1/universal/grok/latest/actions/delete-previous-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/grok/latest/actions/delete-previous-response?connectionId=$CONNECTION_ID&responseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "responseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/delete-previous-response?${params}`, {
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
| `responseId` | string | yes | Response identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Grok API returns.

## Native endpoint

Through the native Grok API, this operation is `DELETE /v1/responses/:response_id` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-previous-response.md) for the provider-specific parameters and requirements.

