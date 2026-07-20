# Quo: Delete Webhook By ID

Deletes an existing webhook from Quo.

```
DELETE https://connect.mindcloud.co/v1/universal/quo/latest/actions/delete-webhook-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/quo/latest/actions/delete-webhook-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/delete-webhook-by-id?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Empty response body. Saved runtime evidence for DELETE /webhooks/:id returned HTTP 204 No Content. |

## Native endpoint

Through the native Quo API, this operation is `DELETE /webhooks/:id` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-by-id.md) for the provider-specific parameters and requirements.

