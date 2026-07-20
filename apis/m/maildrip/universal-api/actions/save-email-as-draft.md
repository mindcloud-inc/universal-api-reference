# Maildrip: Save email as draft



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/save-email-as-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/save-email-as-draft" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailId": "ava@example.com",
  "subject": "string",
  "body": "string",
  "typeOfMail": "string",
  "emailInterval": 1,
  "replyTo": "string",
  "from": "string",
  "groups[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/save-email-as-draft', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailId": "ava@example.com",
    "subject": "string",
    "body": "string",
    "typeOfMail": "string",
    "emailInterval": 1,
    "replyTo": "string",
    "from": "string",
    "groups[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailId` | string | yes | ID of the email to save as draft |
| `subject` | string | yes |  |
| `body` | string | yes |  |
| `typeOfMail` | string | yes |  |
| `emailInterval` | number | yes |  |
| `replyTo` | string | yes |  |
| `from` | string | yes |  |
| `groups[]` | array<string> | yes | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdInstantEmail": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdInstantEmail` | object |  |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/instant-emails/save-as-draft/{emailId}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-email-as-draft.md) for the provider-specific parameters and requirements.

