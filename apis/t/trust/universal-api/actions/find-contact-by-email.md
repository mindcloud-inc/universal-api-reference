# Trust: Find Contact By Email

Finds contacts in Trust by email address.

```
GET https://connect.mindcloud.co/v1/universal/trust/latest/actions/find-contact-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trust/latest/actions/find-contact-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trust/latest/actions/find-contact-by-email?${params}`, {
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
| `email` | string | yes | The email address of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "imageUrl": "https://example.com",
      "lastName": "Chen",
      "phone": "string",
      "typeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `created` | date |  |
| `customerId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `imageUrl` | string |  |
| `lastName` | string |  |
| `phone` | string |  |
| `typeId` | string |  |

## Native endpoint

Through the native Trust API, this operation is `GET /contacts` (base URL `https://api.usetrust.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-contact-by-email.md) for the provider-specific parameters and requirements.

