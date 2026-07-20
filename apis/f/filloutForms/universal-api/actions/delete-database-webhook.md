# Fillout Forms: Delete Database Webhook

Deletes a database webhook from Fillout.

```
DELETE https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-database-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-database-webhook?connectionId=$CONNECTION_ID&databaseId=base_abc123&webhookId=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "base_abc123",
  "webhookId": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/delete-database-webhook?${params}`, {
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
| `databaseId` | string | yes | The unique identifier of the database. Example: `base_abc123`. |
| `webhookId` | number | yes | The unique identifier of the webhook. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Deletion status message. |
| `success` | boolean | Whether the webhook was deleted successfully. |

## Native endpoint

Through the native Fillout Forms API, this operation is `DELETE https://tables.fillout.com/api/v1/bases/:databaseId/webhooks/:webhookId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-database-webhook.md) for the provider-specific parameters and requirements.

