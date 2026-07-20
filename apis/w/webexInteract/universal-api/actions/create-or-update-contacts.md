# Webex Interact: Create or update contacts

Creates or updates contacts in Webex Interact.

```
POST https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/create-or-update-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/create-or-update-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "string",
  "merge_type": "string",
  "contacts": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/create-or-update-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": "string",
    "merge_type": "string",
    "contacts": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string | no | URL to receive a webhook when contact creation processing completes. |
| `correlation_id` | string | no | Correlation ID returned on the contact completion callback webhook. |
| `list_id` | string | yes | ID of the list where contacts are added or updated. |
| `phone_region` | string | no | Default phone region, such as GB. |
| `merge_type` | string | yes | Merge behavior: skipDuplicates, allowDuplicates, mergeByPhoneNumberInList, or mergeByWhatsappIdInList. |
| `contacts` | list<object> | yes | Array of contact objects. Each contact must include phone_number or whatsapp_number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "list_id": "string",
      "list_name": "Ava Chen",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `list_id` | string |  |
| `list_name` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Webex Interact API, this operation is `POST /contacts/v1/contacts` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-contacts.md) for the provider-specific parameters and requirements.

