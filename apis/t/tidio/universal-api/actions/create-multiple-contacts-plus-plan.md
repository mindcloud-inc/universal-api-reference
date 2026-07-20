# Tidio: Create Multiple Contacts [Plus plan]

Creates multiple contacts in the Tidio workspace.

```
POST https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-multiple-contacts-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-multiple-contacts-plus-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts": {},
  "contacts[].distinctId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tidio/latest/actions/create-multiple-contacts-plus-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts": {},
    "contacts[].distinctId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts` | list<object> | yes | List of contacts to create. Maximum 100 per request. |
| `contacts[].distinctId` | string | yes | External-system identifier for the contact. |
| `contacts[].email` | string | no | Contact email address. |
| `contacts[].firstName` | string | no | Contact first name. |
| `contacts[].lastName` | string | no | Contact last name. |
| `contacts[].phone` | string | no | Contact phone number. |
| `contacts[].emailConsent` | string | no | Newsletter consent status for the contact. |
| `contacts[].properties` | list<object> | no | Optional list of custom contact properties. |
| `contacts[].properties[].name` | string | no | Name of the contact property. |
| `contacts[].properties[].value` | string | no | Value of the contact property. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> |  |
| `contacts[]` | object |  |
| `contacts[].city` | string | City of the contact |
| `contacts[].country` | string | Country of the contact in ISO 3166 Alpha-2 format (uppercase) |
| `contacts[].createdAt` | date | Creation date of the contact |
| `contacts[].distinctId` | string | ID of the contact in external system |
| `contacts[].email` | string | Email address of the contact |
| `contacts[].emailConsent` | string | This field indicates if contact agreed to newsletter subscription |
| `contacts[].firstName` | string | First name of the contact |
| `contacts[].id` | string | ID of the contact |
| `contacts[].instagramId` | string | ❗️ <strong>Deprecated:</strong> it always returns null. Will be removed in the next version.  Instagram ID of the contact |
| `contacts[].language` | string | Language of the contact in ISO 639-1 format (lowercase) |
| `contacts[].lastName` | string | Last name of the contact |
| `contacts[].messengerId` | string | ❗️ <strong>Deprecated:</strong> it always returns null. Will be removed in the next version.  Messenger ID of the contact |
| `contacts[].phone` | string | Phone number of the contact |
| `contacts[].properties` | array<object> |  |
| `contacts[].properties[]` | object |  |
| `contacts[].properties[].name` | string | Contact property name |
| `contacts[].properties[].value` | string | Contact property value |

## Native endpoint

Through the native Tidio API, this operation is `POST /contacts/batch` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-contacts-plus-plan.md) for the provider-specific parameters and requirements.

