# RAYNET CRM: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/get-contact?connectionId=$CONNECTION_ID&personId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/get-contact?${params}`, {
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
| `personId` | number | yes | The Raynet contact identifier from the /person/{personId}/ path. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeUserAccount": true,
      "contactInfo": {
        "email": "ava@example.com",
        "email2": "ava@example.com",
        "tel1": "string"
      },
      "firstName": "Ava",
      "id": 1,
      "keyman": true,
      "lastName": "Chen",
      "owner": {
        "fullName": "Ava Chen"
      },
      "primaryRelationship": {
        "company": {
          "id": 1,
          "name": "Ava Chen"
        },
        "type": "string"
      },
      "privateAddress": {
        "country": "string",
        "countryCode": "string"
      },
      "rowInfo": {
        "createdAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeUserAccount` | boolean | Whether the contact has an active user account. |
| `contactInfo.email` | string | Primary email address. |
| `contactInfo.email2` | string | Secondary email address. |
| `contactInfo.tel1` | string | Primary phone number. |
| `firstName` | string | Contact first name. |
| `id` | number | Raynet contact identifier. |
| `keyman` | boolean | Whether the contact is marked as keyman. |
| `lastName` | string | Contact last name. |
| `owner.fullName` | string | Assigned owner full name. |
| `primaryRelationship.company.id` | number | Primary company identifier. |
| `primaryRelationship.company.name` | string | Primary company name. |
| `primaryRelationship.type` | string | Primary relationship type. |
| `privateAddress.country` | string | Private address country. |
| `privateAddress.countryCode` | string | Private address country code. |
| `rowInfo.createdAt` | date | Record creation timestamp. |

## Native endpoint

Through the native RAYNET CRM API, this operation is `GET person/:personId/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

