# Tidio: List Contacts [Plus plan]

Retrieves contacts from the Tidio workspace.

```
GET https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-contacts-plus-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tidio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-contacts-plus-plan?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tidio/latest/actions/list-contacts-plus-plan?${params}`, {
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
| `email` | string | no | Filter contacts by email address. |

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
      ],
      "meta": {
        "cursor": "string",
        "limit": 1
      }
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
| `meta` | object |  |
| `meta.cursor` | string | Value to fetch the next page. Null means the page is the last one. |
| `meta.limit` | number | How many items were displayed on list |

## Native endpoint

Through the native Tidio API, this operation is `GET /contacts` (base URL `https://api.tidio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts-plus-plan.md) for the provider-specific parameters and requirements.

