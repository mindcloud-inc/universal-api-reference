# Wooxy: Send Batch Triggered Email

Sends batch triggered emails through Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-batch-triggered-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-batch-triggered-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactListId": "CONTACT_LIST_ID",
  "templateId": "69d68c4e4f47c8e4a60ee99f",
  "contacts[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-batch-triggered-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactListId": "CONTACT_LIST_ID",
    "templateId": "69d68c4e4f47c8e4a60ee99f",
    "contacts[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactListId` | string | yes | The Wooxy contact list ID. The list must already exist in your account. Example: `CONTACT_LIST_ID`. |
| `templateId` | string | yes | The Wooxy template ID to send. Example: `69d68c4e4f47c8e4a60ee99f`. |
| `contacts[]` | array<object> | yes | The contacts array, for example [{"contact":"user@example.com"}]. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/mailer/batch-trigger` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-batch-triggered-email.md) for the provider-specific parameters and requirements.

