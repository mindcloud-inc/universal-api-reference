# SWELLEnterprise: Create Contact

Creates a new contact in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `firstName` | string | yes | The contact's first name. |
| `lastName` | string | yes | The contact's last name. |
| `email` | string | no | The contact's email. |
| `phone` | string | no | The contact's phone. |
| `companyId` | number | no | The company ID. |
| `notes` | string | no | Notes about the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "company": {
          "id": 1,
          "name": "Ava Chen"
        },
        "companyId": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "deletedAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "id": 1,
        "lastName": "Chen",
        "notes": [
          "string"
        ],
        "phone": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "message": "string",
      "meta": {
        "timestamp": "2026-05-07T12:00:00.000Z",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.company.id` | number | The company ID. |
| `data.company.name` | string | The company name. |
| `data.companyId` | number | The company ID linked to the contact. |
| `data.createdAt` | date | When the contact was created. |
| `data.deletedAt` | date | When the contact was deleted. |
| `data.email` | string | The contact's email. |
| `data.firstName` | string | The contact's first name. |
| `data.fullName` | string | The contact's full name. |
| `data.id` | number | The contact ID. |
| `data.lastName` | string | The contact's last name. |
| `data.notes` | array<string> | Notes about the contact. |
| `data.phone` | string | The contact's phone. |
| `data.updatedAt` | date | When the contact was last updated. |
| `message` | string | Success message. |
| `meta.timestamp` | date | Response timestamp. |
| `meta.version` | string | API version. |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /crm/contacts` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

