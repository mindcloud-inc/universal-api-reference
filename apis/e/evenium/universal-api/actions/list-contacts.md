# Evenium: List Contacts

Retrieves contacts from Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-contacts?${params}`, {
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
| `company` | string | no | Only retrieve contacts whose company matches. |
| `email` | string | no | Only retrieve contacts whose email matches. |
| `firstName` | string | no | Only retrieve contacts whose first name matches. |
| `lastName` | string | no | Only retrieve contacts whose last name matches. |
| `since` | string | no | Only retrieve contacts updated after this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactLogin": "string",
      "customId": "string",
      "email": "ava@example.com",
      "fields": [
        {}
      ],
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "lastUpdate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactLogin` | string | Evenium-generated contact login code. |
| `customId` | string | External custom identifier for the contact. |
| `email` | string | Contact email address. |
| `fields` | array<object> | Additional Evenium contact fields. |
| `firstName` | string | Contact first name. |
| `id` | number | Evenium contact ID. |
| `lastName` | string | Contact last name. |
| `lastUpdate` | date | Last modification timestamp. |

## Native endpoint

Through the native Evenium API, this operation is `GET /contacts` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

