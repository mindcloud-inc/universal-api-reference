# noCRM.io: Create Client Folder

Creates a new client folder in noCRM.io.

```
POST https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/create-client-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a noCRM.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/create-client-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/noCRMio/latest/actions/create-client-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Client folder name. |
| `description` | string | no | Client folder description. |
| `userId` | string | no | User email or ID to assign the folder to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "extendedInfo": {
        "fields": {
          "address": {},
          "city": {},
          "companyId": {},
          "country": {},
          "custom1": {},
          "custom2": {},
          "custom3": {},
          "custom4": {},
          "custom5": {},
          "email": {},
          "fax": {},
          "firstName": {},
          "fullName": {},
          "job": {},
          "lastName": {},
          "mobile": {},
          "phone": {},
          "state": {},
          "vat": {},
          "web": {},
          "zipcode": {}
        },
        "fieldsByName": {
          "billingAddress": {},
          "deliveryAddress": {},
          "vATNumber": {}
        },
        "permalink": "https://example.com",
        "user": {
          "email": "ava@example.com",
          "firstname": "Ava",
          "id": 1,
          "lastname": "Chen",
          "mobilePhone": {},
          "phone": {}
        }
      },
      "id": 1,
      "isActive": true,
      "name": "Ava Chen",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `extendedInfo` | object |  |
| `extendedInfo.fields` | object |  |
| `extendedInfo.fields.address` | object |  |
| `extendedInfo.fields.city` | object |  |
| `extendedInfo.fields.companyId` | object |  |
| `extendedInfo.fields.country` | object |  |
| `extendedInfo.fields.custom1` | object |  |
| `extendedInfo.fields.custom2` | object |  |
| `extendedInfo.fields.custom3` | object |  |
| `extendedInfo.fields.custom4` | object |  |
| `extendedInfo.fields.custom5` | object |  |
| `extendedInfo.fields.email` | object |  |
| `extendedInfo.fields.fax` | object |  |
| `extendedInfo.fields.firstName` | object |  |
| `extendedInfo.fields.fullName` | object |  |
| `extendedInfo.fields.job` | object |  |
| `extendedInfo.fields.lastName` | object |  |
| `extendedInfo.fields.mobile` | object |  |
| `extendedInfo.fields.phone` | object |  |
| `extendedInfo.fields.state` | object |  |
| `extendedInfo.fields.vat` | object |  |
| `extendedInfo.fields.web` | object |  |
| `extendedInfo.fields.zipcode` | object |  |
| `extendedInfo.fieldsByName` | object |  |
| `extendedInfo.fieldsByName.billingAddress` | object |  |
| `extendedInfo.fieldsByName.deliveryAddress` | object |  |
| `extendedInfo.fieldsByName.vATNumber` | object |  |
| `extendedInfo.permalink` | string |  |
| `extendedInfo.user` | object |  |
| `extendedInfo.user.email` | string |  |
| `extendedInfo.user.firstname` | string |  |
| `extendedInfo.user.id` | number |  |
| `extendedInfo.user.lastname` | string |  |
| `extendedInfo.user.mobilePhone` | object |  |
| `extendedInfo.user.phone` | object |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native noCRM.io API, this operation is `POST /clients` (base URL `{{credentials.baseUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-folder.md) for the provider-specific parameters and requirements.

