# Woodpecker.co: Update Mailbox

Updates a mailbox in your Woodpecker account.

```
PUT https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/update-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woodpecker.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/update-mailbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "smtpMailboxId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/update-mailbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "smtpMailboxId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `smtpMailboxId` | number | yes | SMTP mailbox ID from Woodpecker. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Woodpecker.co API returns.

## Native endpoint

Through the native Woodpecker.co API, this operation is `PATCH /rest/v2/mailboxes/[:smtp_mailbox_id]` (base URL `https://api.woodpecker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mailbox.md) for the provider-specific parameters and requirements.

