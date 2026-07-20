# MailUp: Create Email

Creates a new email message in MailUp.

```
POST https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/create-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/create-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idList": 1,
  "subject": "string",
  "content": "string",
  "trackingInfo": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailUp/latest/actions/create-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idList": 1,
    "subject": "string",
    "content": "string",
    "trackingInfo": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idList` | number | yes |  |
| `subject` | string | yes |  |
| `content` | string | yes |  |
| `notes` | string | no |  |
| `structure` | string | no |  |
| `useDynamicField` | boolean | no |  |
| `embed` | boolean | no |  |
| `isConfirmation` | boolean | no |  |
| `preHeader` | string | no |  |
| `trackingInfo` | object | yes | MailUp tracking configuration object, for example {"Enabled":true,"Protocols":["http:","https:","ftp:","news:"],"CustomParams":""}. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreationDate": "string",
      "idList": 1,
      "idMessage": 1,
      "Notes": "string",
      "Subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreationDate` | string |  |
| `idList` | number |  |
| `idMessage` | number |  |
| `Notes` | string |  |
| `Subject` | string |  |

## Native endpoint

Through the native MailUp API, this operation is `POST Console/List/:id_List/Email` (base URL `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email.md) for the provider-specific parameters and requirements.

