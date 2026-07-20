# Fleetio: Retrieve Contact

Retrieves a specific contact from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-contact?${params}`, {
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
| `id` | string | yes | The id of the relevant record |
| `expand` | array<string> | no | Additional attributes that should be returned in the response. Available: `group` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountMembershipId": {},
      "archivedAt": {},
      "birthDate": {},
      "city": {},
      "commentsCount": 1,
      "country": {},
      "createdAt": "string",
      "defaultImageUrl": {},
      "documentsCount": 1,
      "email": {},
      "employee": true,
      "employeeNumber": {},
      "firstName": "Ava",
      "groupId": {},
      "groupName": {},
      "homePhoneNumber": {},
      "hourlyLaborRate": {},
      "id": 1,
      "imagesCount": 1,
      "jobTitle": {},
      "lastApiRequest": {},
      "lastMobileAppAccess": {},
      "lastName": {},
      "lastWebAccess": {},
      "leaveDate": {},
      "licenseClass": {},
      "licenseExpiration": {},
      "licenseNumber": {},
      "licenseState": {},
      "middleName": {},
      "mobilePhoneNumber": {},
      "name": "Ava Chen",
      "otherPhoneNumber": {},
      "postalCode": {},
      "region": {},
      "startDate": {},
      "streetAddress": {},
      "streetAddressLine2": {},
      "technician": true,
      "updatedAt": "string",
      "user": {},
      "vehicleOperator": {},
      "workPhoneNumber": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountMembershipId` | object |  |
| `archivedAt` | object |  |
| `birthDate` | object |  |
| `city` | object |  |
| `commentsCount` | number |  |
| `country` | object |  |
| `createdAt` | string |  |
| `defaultImageUrl` | object |  |
| `documentsCount` | number |  |
| `email` | object |  |
| `employee` | boolean |  |
| `employeeNumber` | object |  |
| `firstName` | string |  |
| `groupId` | object |  |
| `groupName` | object |  |
| `homePhoneNumber` | object |  |
| `hourlyLaborRate` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `jobTitle` | object |  |
| `lastApiRequest` | object |  |
| `lastMobileAppAccess` | object |  |
| `lastName` | object |  |
| `lastWebAccess` | object |  |
| `leaveDate` | object |  |
| `licenseClass` | object |  |
| `licenseExpiration` | object |  |
| `licenseNumber` | object |  |
| `licenseState` | object |  |
| `middleName` | object |  |
| `mobilePhoneNumber` | object |  |
| `name` | string |  |
| `otherPhoneNumber` | object |  |
| `postalCode` | object |  |
| `region` | object |  |
| `startDate` | object |  |
| `streetAddress` | object |  |
| `streetAddressLine2` | object |  |
| `technician` | boolean |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `vehicleOperator` | object |  |
| `workPhoneNumber` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET contacts/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

