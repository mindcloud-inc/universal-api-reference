# InstantCard: Create Contact

Creates a new contact in InstantCard.

```
POST https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "20003827",
  "fullName": "MindCloud Contact Bot",
  "email": "api+contact@instantcard.net"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "20003827",
    "fullName": "MindCloud Contact Bot",
    "email": "api+contact@instantcard.net"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `altEmail` | string | no | Alternate email. |
| `altPhoneNumber` | string | no | Alternate phone number. |
| `organizationId` | number | yes | Organization ID from InstantCard. Example: `20003827`. |
| `fullName` | string | yes | Contact full name. Example: `MindCloud Contact Bot`. |
| `email` | string | yes | Contact email. Example: `api+contact@instantcard.net`. |
| `phoneNumber` | string | no | Phone number. Example: `555-450-9908`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "alt_email": "ava@example.com",
      "alt_phone_number": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "organization_id": 1,
      "phone_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> | Related addresses. |
| `alt_email` | string | Alternate email address. |
| `alt_phone_number` | string | Alternate phone number. |
| `email` | string | Primary email address. |
| `full_name` | string | Contact full name. |
| `id` | number | Contact ID. |
| `organization_id` | number | Organization ID. |
| `phone_number` | string | Primary phone number. |

## Native endpoint

Through the native InstantCard API, this operation is `POST /api/v2/organizations/:organizationId/contacts` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

