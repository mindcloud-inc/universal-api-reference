# MailRook Email Validation: Submit Validation Batch

Submits a batch of email addresses for validation in MailRook.

```
POST https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/submit-validation-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailRook Email Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/submit-validation-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/submit-validation-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Array of email addresses to validate in one batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | MailRook response code. |
| `data` | object | Created batch metadata including the list identifier. |
| `message` | string | MailRook response message. |

## Native endpoint

Through the native MailRook Email Validation API, this operation is `POST /validate/batch` (base URL `https://api.mailrook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-validation-batch.md) for the provider-specific parameters and requirements.

