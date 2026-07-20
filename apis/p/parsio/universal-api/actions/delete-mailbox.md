# Parsio: Delete Mailbox



```
DELETE https://connect.mindcloud.co/v1/universal/parsio/latest/actions/delete-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parsio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/parsio/latest/actions/delete-mailbox?connectionId=$CONNECTION_ID&mailboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parsio/latest/actions/delete-mailbox?${params}`, {
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
| `mailboxId` | string | yes | Parsio mailbox ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Parsio API returns.

## Native endpoint

Through the native Parsio API, this operation is `DELETE /mailboxes/:mailbox_id` (base URL `https://api.parsio.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-mailbox.md) for the provider-specific parameters and requirements.

