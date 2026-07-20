# respond.io: Create Contact

Creates a new contact in respond.io.

```
POST https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "firstName": "Ava",
  "customFields[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "firstName": "Ava",
    "customFields[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | Contact identifier (email: or phone:). |
| `firstName` | string | yes | Contact first name. |
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
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |

## Native endpoint

Through the native respond.io API, this operation is `POST /contact/:identifier` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

