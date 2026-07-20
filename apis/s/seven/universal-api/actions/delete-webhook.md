# Seven: Delete Webhook

Deletes a webhook from Seven.

```
DELETE https://connect.mindcloud.co/v1/universal/seven/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/seven/latest/actions/delete-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/delete-webhook?${params}`, {
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
| `id` | number | no | The ID of the webhook you want to delete. |
| `targetUrl` | string | no | Destination address of your webhook. |
| `eventType` | string | no | Type of event for which you would like to receive a webhook. |
| `requestMethod` | string | no | Request method in which you would like to receive the webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "error_message": "string",
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `error_message` | string |  |
| `id` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `DELETE /hooks` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

