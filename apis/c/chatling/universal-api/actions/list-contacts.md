# Chatling: List Contacts

Retrieves contacts from Chatling.

```
GET https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-contacts?connectionId=$CONNECTION_ID&chatbotId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatling/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatbotId` | string | yes | The chatbot ID. |
| `sort` | string | no | The sort order for the contacts list. Default: `date_desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": "string",
      "jobTitle": "string",
      "name": "Ava Chen",
      "phone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | The company name of the contact. |
| `createdAt` | string | The date and time when the contact was created. |
| `email` | string | The email address of the contact. |
| `id` | string | The unique identifier of the contact. |
| `jobTitle` | string | The job title of the contact. |
| `name` | string | The name of the contact. |
| `phone` | string | The phone number of the contact. |
| `website` | string | The website URL of the contact. |

## Native endpoint

Through the native Chatling API, this operation is `GET /chatbots/:chatbotId/contacts` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

