# MailUp: Get Email Send History

Retrieves send history for a MailUp email.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-email-send-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-email-send-history?connectionId=$CONNECTION_ID&idList=1&idMessage=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idList": "1",
  "idMessage": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-email-send-history?${params}`, {
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
| `idMessage` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "id": 1,
      "idMessage": 1,
      "kbTransferred": 1,
      "recipients": 1,
      "senderEmail": "ava@example.com",
      "senderName": "Ava Chen",
      "startDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `id` | number |  |
| `idMessage` | number |  |
| `kbTransferred` | number |  |
| `recipients` | number |  |
| `senderEmail` | string |  |
| `senderName` | string |  |
| `startDate` | string |  |

## Native endpoint

Through the native MailUp API, this operation is `GET Console/List/:id_List/Email/:id_Message/SendHistory` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-send-history.md) for the provider-specific parameters and requirements.

