# Sender: Send Transactional Email Without Template



```
POST https://connect.mindcloud.co/v1/universal/sender/latest/actions/send-transactional-email-without-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sender/latest/actions/send-transactional-email-without-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "[object Object]",
  "to": "[object Object]",
  "subject": "Your verification code"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/send-transactional-email-without-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "[object Object]",
    "to": "[object Object]",
    "subject": "Your verification code"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | object | yes | Sender object containing email and name. Example: `[object Object]`. |
| `to` | object | yes | Recipient object containing required email and optional name. Example: `[object Object]`. |
| `subject` | string | yes | Subject line of the email. Example: `Your verification code`. |
| `text` | string | no | Plain-text version of the email body. Example: `Plain text body`. |
| `html` | string | no | HTML version of the email body. Example: `<p>HTML body</p>`. |
| `headers` | object | no | Optional headers to include. Example: `[object Object]`. |
| `variables` | object | no | Key-value variables for personalization. Example: `[object Object]`. |
| `attachments` | object | no | Filename-to-URL attachment map. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailId": "ava@example.com",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Sender API, this operation is `POST /message/send` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-email-without-template.md) for the provider-specific parameters and requirements.

