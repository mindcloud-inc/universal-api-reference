# Tidio: Get Contact [Plus plan]

Retrieves a contact from the Tidio workspace.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-plus-plan?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/get-contact-plus-plan?${params}`, {
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
| `contactId` | string | yes | The Tidio contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "distinctId": "string",
      "email": "ava@example.com",
      "emailConsent": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "instagramId": "string",
      "language": "string",
      "lastName": "Chen",
      "messengerId": "string",
      "phone": "string",
      "properties": [
        {
          "name": "Ava Chen",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | City of the contact |
| `country` | string | Country of the contact in ISO 3166 Alpha-2 format (uppercase) |
| `createdAt` | date | Creation date of the contact |
| `distinctId` | string | ID of the contact in external system |
| `email` | string | Email address of the contact |
| `emailConsent` | string | This field indicates if contact agreed to newsletter subscription |
| `firstName` | string | First name of the contact |
| `id` | string | ID of the contact |
| `instagramId` | string | ❗️ <strong>Deprecated:</strong> it always returns null. Will be removed in the next version.  Instagram ID of the contact |
| `language` | string | Language of the contact in ISO 639-1 format (lowercase) |
| `lastName` | string | Last name of the contact |
| `messengerId` | string | ❗️ <strong>Deprecated:</strong> it always returns null. Will be removed in the next version.  Messenger ID of the contact |
| `phone` | string | Phone number of the contact |
| `properties` | array<object> |  |
| `properties[]` | object |  |
| `properties[].name` | string | Contact property name |
| `properties[].value` | string | Contact property value |

## Native endpoint

Through the native Tidio API, this operation is `GET /contacts/{contactId}` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-plus-plan.md) for the provider-specific parameters and requirements.

