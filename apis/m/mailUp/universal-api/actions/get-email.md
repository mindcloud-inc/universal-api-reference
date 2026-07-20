# MailUp: Get Email

Retrieves an email message from MailUp.

```
GET https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-email?connectionId=$CONNECTION_ID&idList=1&idMessage=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idList": "1",
  "idMessage": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/get-email?${params}`, {
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
      "attachments": [
        {}
      ],
      "content": "string",
      "creationDate": "string",
      "embed": true,
      "fields": [
        {}
      ],
      "idList": 1,
      "idMessage": 1,
      "isConfirmation": true,
      "notes": "string",
      "preHeader": "string",
      "structure": "string",
      "subject": "string",
      "tags": [
        {}
      ],
      "trackingInfo": {},
      "useDynamicField": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `content` | string |  |
| `creationDate` | string |  |
| `embed` | boolean |  |
| `fields` | array<object> |  |
| `idList` | number |  |
| `idMessage` | number |  |
| `isConfirmation` | boolean |  |
| `notes` | string |  |
| `preHeader` | string |  |
| `structure` | string |  |
| `subject` | string |  |
| `tags` | array<object> |  |
| `trackingInfo` | object |  |
| `useDynamicField` | boolean |  |

## Native endpoint

Through the native MailUp API, this operation is `GET Console/List/:id_List/Email/:id_Message` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email.md) for the provider-specific parameters and requirements.

