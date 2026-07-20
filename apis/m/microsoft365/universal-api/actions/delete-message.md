# Microsoft 365: Delete Message

Deletes a message from Microsoft 365.

```
DELETE https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/delete-message?connectionId=$CONNECTION_ID&messageId=AAMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "AAMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/delete-message?${params}`, {
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
| `messageId` | string | yes | The ID of the Outlook message to delete. Example: `AAMkAG...`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 API returns.

## Native endpoint

Through the native Microsoft 365 API, this operation is `DELETE /v1.0/me/messages/{{messageId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

