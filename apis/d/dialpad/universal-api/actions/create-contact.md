# Dialpad: Create Contact

Creates a new contact in Dialpad.

```
POST https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "first_name": "Ava",
  "last_name": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "first_name": "Ava",
    "last_name": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company_name` | string | no | The contact's company name. |
| `emails[]` | array<string> | no | The contact's emails. The first email in the list is the contact's primary email. |
| `extension` | string | no | The contact's extension number. |
| `first_name` | string | yes | The contact's first name. |
| `job_title` | string | no | The contact's job title. |
| `last_name` | string | yes | The contact's last name. |
| `owner_id` | string | no | If provided, a local contact will be created for this user. |
| `phones[]` | array<string> | no | The contact's phone numbers. The first number in the list is the contact's primary phone. |
| `urls[]` | array<string> | no | A list of websites associated with or belonging to this contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "ownerId": "string",
      "primaryEmail": "ava@example.com",
      "primaryPhone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `ownerId` | string |  |
| `primaryEmail` | string |  |
| `primaryPhone` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `POST /contacts` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

