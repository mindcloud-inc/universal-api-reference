# MailUp: Import Recipients

Imports recipients into a MailUp list.

```
POST https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/import-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/import-recipients" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idList": 1,
  "recipients": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/import-recipients', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idList": 1,
    "recipients": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idList` | number | yes |  |
| `recipients` | object | yes | JSON array of MailUp recipient objects. Each item should use MailUp keys such as Email, Name, MobileNumber, and MobilePrefix. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MailUp API returns.

## Native endpoint

Through the native MailUp API, this operation is `POST Console/List/:id_List/Recipients` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-recipients.md) for the provider-specific parameters and requirements.

