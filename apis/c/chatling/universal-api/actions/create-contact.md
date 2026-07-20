# Chatling: Create Contact

Creates a new contact in Chatling.

```
POST https://connect.mindcloud.co/v1/universal/chatling/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatling/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatbotId` | string | yes | The chatbot ID. |
| `properties.firstName` | string | no | The contact's first name. Example: `John`. |
| `properties.lastName` | string | no | The contact's last name. Example: `Doe`. |
| `properties.email` | string | no | The contact's email address. Example: `codex-stage3-contact+20260320@example.com`. |
| `properties.phone` | string | no | The contact's phone number. Example: `1234567890`. |
| `properties.jobTitle` | string | no | The contact's job title. Example: `Software Engineer`. |
| `properties.companyName` | string | no | The contact's company name. Example: `Acme Inc`. |
| `properties.websiteUrl` | string | no | The contact's website URL. Example: `https://acme.com`. |
| `properties.industry` | string | no | The contact's industry. Example: `Technology`. |
| `properties.address` | string | no | The contact's address. Example: `123 Main St`. |
| `properties.city` | string | no | The contact's city. Example: `New York`. |
| `properties.state` | string | no | The contact's state. Example: `NY`. |
| `properties.postalCode` | string | no | The contact's postal code. Example: `10001`. |
| `properties.country` | string | no | The contact's country. Example: `USA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Contact ID returned by Chatling after a successful contact creation. |

## Native endpoint

Through the native Chatling API, this operation is `POST /chatbots/:chatbotId/contacts` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

