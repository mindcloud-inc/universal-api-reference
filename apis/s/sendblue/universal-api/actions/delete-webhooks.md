# Sendblue: Delete Webhooks

Deletes webhooks from Sendblue.

```
DELETE https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-webhooks?connectionId=$CONNECTION_ID&webhooks%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhooks[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-webhooks?${params}`, {
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
| `webhooks[]` | array<string> | yes | Webhook URLs to delete. Accepts multiple values as an array. |
| `type` | string | no | The webhook event type to delete from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `DELETE /api/account/webhooks` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhooks.md) for the provider-specific parameters and requirements.

