# ActiveTrail: Send Email Operational Message to Contacts

Sends an operational email to contacts in ActiveTrail.

```
POST https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/send-email-operational-message-to-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveTrail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/send-email-operational-message-to-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "design": {},
  "details": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/send-email-operational-message-to-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "design": {},
    "details": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bcc` | object | no | BCC emails. |
| `bcc.bcc_emails[]` | array<string> | no |  |
| `contact_package[]` | array<object> | no | Email addresses with per-contact key/value pairs. |
| `contact_package[].contact` | object | no |  |
| `contact_package[].contact.email` | string | no |  |
| `contact_package[].contact.first_name` | string | no |  |
| `contact_package[].contact.last_name` | string | no |  |
| `contact_package[].contact.sms` | string | no |  |
| `contact_package[].pairs[]` | array<object> | no |  |
| `contact_package[].pairs[].key` | string | no |  |
| `contact_package[].pairs[].value` | string | no |  |
| `design` | object | yes | Message design. |
| `design.add_print_button` | boolean | no |  |
| `design.add_Statistics` | boolean | no |  |
| `design.content` | string | no |  |
| `design.language_type` | string | no |  |
| `design.template_id` | number | no |  |
| `details` | object | yes | Message details. |
| `details.classification` | string | no |  |
| `details.name` | string | no |  |
| `details.subject` | string | no |  |
| `details.user_profile_fromname` | string | no |  |
| `details.user_profile_id` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveTrail API returns.

## Native endpoint

Through the native ActiveTrail API, this operation is `POST /OperationalMessage/Contacts` (base URL `https://webapi.mymarketing.co.il/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-email-operational-message-to-contacts.md) for the provider-specific parameters and requirements.

