# Maildrip: Send onboarding test mail using dedicated test domains



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-onboarding-test-mail-using-dedicated-test-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-onboarding-test-mail-using-dedicated-test-domains" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/send-onboarding-test-mail-using-dedicated-test-domains', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes |  |
| `body` | string | yes |  |
| `recipients[]` | array<string> | no | Accepts multiple values as an array. |
| `fromName` | string | no |  |
| `replyTo` | string | no |  |
| `attachments[]` | array<object> | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "invalidEmails": [
        "ava@example.com"
      ],
      "message": "string",
      "provider": "string",
      "sentTo": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `invalidEmails` | array<string> |  |
| `message` | string |  |
| `provider` | string |  |
| `sentTo` | array<string> |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/onboarding/test-email` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-onboarding-test-mail-using-dedicated-test-domains.md) for the provider-specific parameters and requirements.

