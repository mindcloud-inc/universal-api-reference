# MailUp: Unsubscribe Recipient

Unsubscribes a recipient from a MailUp list.

```
DELETE https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/unsubscribe-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/unsubscribe-recipient?connectionId=$CONNECTION_ID&idList=1&idRecipient=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idList": "1",
  "idRecipient": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/unsubscribe-recipient?${params}`, {
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
| `idList` | number | yes |  |
| `idRecipient` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MailUp API returns.

## Native endpoint

Through the native MailUp API, this operation is `DELETE Console/List/:id_List/Unsubscribe/:id_Recipient` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-recipient.md) for the provider-specific parameters and requirements.

