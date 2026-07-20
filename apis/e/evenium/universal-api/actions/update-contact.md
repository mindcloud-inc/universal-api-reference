# Evenium: Update Contact

Updates an existing contact in Evenium.

```
PUT https://connect.mindcloud.co/v1/universal/evenium/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evenium/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | The Evenium Company. |
| `contactId` | number | yes | The Evenium Contact ID. |
| `email` | string | no | The Evenium Email. |

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

Through the native Evenium API, this operation is `PUT /contacts/:contactId` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

