# Resend: Retrieve Contact

Retrieves a contact from Resend.

```
GET https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=e169aa45-1ecf-4183-9955-b1499d5701d3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e169aa45-1ecf-4183-9955-b1499d5701d3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/retrieve-contact?${params}`, {
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
| `id` | string | yes | Example: `e169aa45-1ecf-4183-9955-b1499d5701d3`. |
| `email` | list | no | Example: `steve.wozniak@gmail.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "object": "string",
      "properties": {},
      "unsubscribed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the contact was created. |
| `email` | string | Contact email address. |
| `firstName` | string | Contact first name, when present. |
| `id` | string | Contact identifier. |
| `lastName` | string | Contact last name, when present. |
| `object` | string | Object type identifier. |
| `properties` | object | Custom contact properties. |
| `unsubscribed` | boolean | Whether the contact is unsubscribed. |

## Native endpoint

Through the native Resend API, this operation is `GET /contacts/:id` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

