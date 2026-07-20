# Evenium: Create Contact

Creates a new contact in Evenium.

```
POST https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customId": "string",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evenium/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customId": "string",
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | The Evenium Company. |
| `customId` | string | yes | The Evenium Custom ID. |
| `email` | string | yes | The Evenium Email. |
| `firstName` | string | yes | The Evenium First Name. |
| `lastName` | string | yes | The Evenium Last Name. |

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

Through the native Evenium API, this operation is `POST /contacts` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

