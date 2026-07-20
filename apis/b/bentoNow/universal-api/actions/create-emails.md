# Bento Now: Create Emails

Queues transactional emails in Bento Now.

```
POST https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[].from": "ava@example.com",
  "emails[].htmlBody": "ava@example.com",
  "emails[].subject": "ava@example.com",
  "emails[].to": "ava@example.com",
  "emails[].transactional": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-emails', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[].from": "ava@example.com",
    "emails[].htmlBody": "ava@example.com",
    "emails[].subject": "ava@example.com",
    "emails[].to": "ava@example.com",
    "emails[].transactional": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[].from` | string | yes |  |
| `emails[].htmlBody` | string | yes |  |
| `emails[].subject` | string | yes |  |
| `emails[].to` | string | yes |  |
| `emails[].transactional` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": 1,
      "results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed` | number |  |
| `results` | number |  |

## Native endpoint

Through the native Bento Now API, this operation is `POST /v1/batch/emails` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-emails.md) for the provider-specific parameters and requirements.

