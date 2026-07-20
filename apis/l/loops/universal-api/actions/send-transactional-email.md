# Loops: Send Transactional Email

Creates a transactional email send in Loops.

```
POST https://connect.mindcloud.co/v1/universal/loops/latest/actions/send-transactional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loops/latest/actions/send-transactional-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "transactionalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loops/latest/actions/send-transactional-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "transactionalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |
| `transactionalId` | string | yes |  |
| `addToAudience` | boolean | no |  |
| `dataVariables` | object | no |  |
| `attachments[]` | array<object> | no |  |
| `attachments[].filename` | string | no |  |
| `attachments[].contentType` | string | no |  |
| `attachments[].data` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether Loops accepted the transactional email send request. |

## Native endpoint

Through the native Loops API, this operation is `POST /transactional` (base URL `https://app.loops.so/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-email.md) for the provider-specific parameters and requirements.

