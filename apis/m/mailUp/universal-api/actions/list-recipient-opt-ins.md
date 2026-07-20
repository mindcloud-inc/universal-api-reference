# MailUp: List Recipient Opt-ins

Retrieves recipient opt-in details from a MailUp list.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-recipient-opt-ins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-recipient-opt-ins?connectionId=$CONNECTION_ID&idList=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idList": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/list-recipient-opt-ins?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "idRecipient": 1,
      "optinDate": "string",
      "optinRequestDate": "string",
      "optinRequestIp": "string",
      "optoutDate": "string",
      "optoutMsgId": 1,
      "optoutSubtype": 1,
      "optoutType": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `idRecipient` | number |  |
| `optinDate` | string |  |
| `optinRequestDate` | string |  |
| `optinRequestIp` | string |  |
| `optoutDate` | string |  |
| `optoutMsgId` | number |  |
| `optoutSubtype` | number |  |
| `optoutType` | number |  |
| `status` | string |  |

## Native endpoint

Through the native MailUp API, this operation is `GET Console/List/:id_List/Recipients/EmailOptins` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recipient-opt-ins.md) for the provider-specific parameters and requirements.

