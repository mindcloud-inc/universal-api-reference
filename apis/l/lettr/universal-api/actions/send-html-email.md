# Lettr: Send HTML Email



```
POST https://connect.mindcloud.co/v1/universal/lettr/latest/actions/send-html-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/send-html-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettr/latest/actions/send-html-email', {
  method: 'POST',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Sender email address. |
| `html` | string | no | HTML email body. |
| `subject` | string | no | Email subject line. |
| `to` | string | no | Recipient email addresses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accepted": 1,
        "rejected": 1,
        "request_id": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Queued email payload. |
| `data.accepted` | number | Accepted recipient count. |
| `data.rejected` | number | Rejected recipient count. |
| `data.request_id` | string | Request ID for the queued email. |
| `message` | string | Email send status message. |

## Native endpoint

Through the native Lettr API, this operation is `POST /emails` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-html-email.md) for the provider-specific parameters and requirements.

