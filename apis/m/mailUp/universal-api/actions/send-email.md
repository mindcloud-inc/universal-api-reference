# MailUp: Send Email

Sends an email message to a MailUp list.

```
POST https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/send-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/send-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idList": 1,
  "idMessage": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/send-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idList": 1,
    "idMessage": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idList` | number | yes |  |
| `idMessage` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Id": 1,
      "idMessage": 1,
      "InvalidRecipients": [
        {}
      ],
      "Sent": 1,
      "UnprocessedRecipients": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Id` | number |  |
| `idMessage` | number |  |
| `InvalidRecipients` | array<object> |  |
| `Sent` | number |  |
| `UnprocessedRecipients` | array<object> |  |

## Native endpoint

Through the native MailUp API, this operation is `POST Console/List/:id_List/Email/:id_Message/Send` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email.md) for the provider-specific parameters and requirements.

