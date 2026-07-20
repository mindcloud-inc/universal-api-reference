# Wooxy: Send Triggered Email

Sends a triggered email through Wooxy.

```
POST https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-triggered-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-triggered-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactListId": "CONTACT_LIST_ID",
  "contact": "apps@mindcloud.co",
  "templateId": "69d68c4e4f47c8e4a60ee99f"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/send-triggered-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactListId": "CONTACT_LIST_ID",
    "contact": "apps@mindcloud.co",
    "templateId": "69d68c4e4f47c8e4a60ee99f"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactListId` | string | yes | The Wooxy contact list ID. The list must already exist in your account. Example: `CONTACT_LIST_ID`. |
| `contact` | string | yes | The recipient email, user ID, or phone number already stored in the contact list. Example: `apps@mindcloud.co`. |
| `templateId` | string | yes | The Wooxy template ID to send. Example: `69d68c4e4f47c8e4a60ee99f`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreBlackList` | boolean | no | Whether to ignore black list status for the send. |

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

Through the native Wooxy API, this operation is `POST v3/mailer/trigger` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-triggered-email.md) for the provider-specific parameters and requirements.

