# Fathom: Delete Webhook

Deletes an existing webhook from Fathom.

```
DELETE https://connect.mindcloud.co/v1/universal/fathom/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fathom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fathom/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fathom/latest/actions/delete-webhook?${params}`, {
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
| `id` | string | yes | Webhook ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Empty response body on successful delete (HTTP 204). |

## Native endpoint

Through the native Fathom API, this operation is `DELETE /webhooks/:id` (base URL `https://api.fathom.ai/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

