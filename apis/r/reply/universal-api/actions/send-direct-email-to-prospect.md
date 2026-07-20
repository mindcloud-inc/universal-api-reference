# Reply: Send Direct Email To Prospect



```
POST https://connect.mindcloud.co/v1/universal/reply/latest/actions/send-direct-email-to-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reply/latest/actions/send-direct-email-to-prospect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "prospectId": 1,
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reply/latest/actions/send-direct-email-to-prospect', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "prospectId": 1,
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | Email body content. |
| `emailAccountId` | number | no | Email account to use for sending the email. |
| `prospectId` | number | yes | Reply prospect identifier. |
| `subject` | string | yes | Email subject line. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sentEmailInfo": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sentEmailInfo` | object | Provider metadata for the sent email. |
| `status` | number | Reply delivery status code for the direct email request. |

## Native endpoint

Through the native Reply API, this operation is `POST /v2/prospects/:prospectid/emails` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-direct-email-to-prospect.md) for the provider-specific parameters and requirements.

