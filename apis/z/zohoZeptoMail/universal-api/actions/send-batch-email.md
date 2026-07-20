# Zoho ZeptoMail: Send Batch Email

Sends transactional emails in bulk through Zoho ZeptoMail.

```
POST https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/send-batch-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/send-batch-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from.address": "string",
  "to[].emailAddress.address": "ava@example.com",
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/send-batch-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from.address": "string",
    "to[].emailAddress.address": "ava@example.com",
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from.address` | string | yes | Verified sender email address. |
| `to[].emailAddress.address` | string | yes | Recipient email address. |
| `subject` | string | yes | Email subject line. |
| `htmlBody` | string | no | HTML email body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "code": "string",
          "message": "string"
        }
      ],
      "message": "string",
      "object": "string",
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].code` | string |  |
| `data[].message` | string |  |
| `message` | string |  |
| `object` | string |  |
| `request_id` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `POST email/batch` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-batch-email.md) for the provider-specific parameters and requirements.

