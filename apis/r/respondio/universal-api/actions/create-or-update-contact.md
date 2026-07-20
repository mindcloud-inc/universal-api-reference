# respond.io: Create Or Update Contact

Finds a contact in respond.io, or creates one if no match is found.

```
PUT https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-or-update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-or-update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "customFields[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-or-update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "customFields[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Contact identifier (id:, email:, or phone:). |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `phone` | string | no | Contact phone number in E.164 format. |
| `email` | string | no | Contact email address. |
| `language` | string | no | ISO 639-1 language code. |
| `profilePic` | string | no | Public URL of the contact avatar. |
| `countryCode` | string | no | ISO 3166-1 alpha-2 country code. |
| `customFields[]` | array<object> | no | Array of custom field updates: [{name, value}]. |
| `customFields[].name` | string | yes | Custom field name (required for each custom field object). |
| `customFields[].value` | string | no | Custom field value for the given custom field name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |

## Native endpoint

Through the native respond.io API, this operation is `POST /contact/create_or_update/:identifier` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-contact.md) for the provider-specific parameters and requirements.

