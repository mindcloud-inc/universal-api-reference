# Webex Interact: Delete sender

Deletes an existing sender from Webex Interact.

```
DELETE https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-sender?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/delete-sender?${params}`, {
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
| `id` | string | yes | Sender ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status_code": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Deleted sender ID. |
| `status_code` | number | HTTP status code returned by the delete request. |
| `success` | boolean | Whether the sender deletion request completed successfully. |

## Native endpoint

Through the native Webex Interact API, this operation is `DELETE /assets/v1/senders/{id}` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sender.md) for the provider-specific parameters and requirements.

