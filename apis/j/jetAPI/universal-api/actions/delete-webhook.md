# JetAPI: Delete Webhook

Deletes an existing webhook from JetAPI.

```
DELETE https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/delete-webhook?${params}`, {
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
| `id` | number | yes | The JetAPI webhook identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta` | object |  |

## Native endpoint

Through the native JetAPI API, this operation is `DELETE /api/v1/webhooks/:id` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

