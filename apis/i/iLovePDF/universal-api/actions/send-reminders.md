# iLovePDF: Send Reminders

Sends signature reminders in iLovePDF.

```
PUT https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/send-reminders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/send-reminders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/send-reminders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "access_code": true,
      "email": "ava@example.com",
      "force_signature_type": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "status": "string",
      "token_requester": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_code` | boolean |  |
| `email` | string |  |
| `force_signature_type` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `status` | string |  |
| `token_requester` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native iLovePDF API, this operation is `POST https://:server/v1/signature/sendReminder/:tokenRequester` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-reminders.md) for the provider-specific parameters and requirements.

