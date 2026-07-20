# Fleetio: List Contacts

Retrieves a list of contacts from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountMembershipId": {},
      "birthDate": {},
      "city": {},
      "commentsCount": 1,
      "country": {},
      "createdAt": "string",
      "defaultImageUrl": "https://example.com",
      "documentsCount": 1,
      "email": {},
      "employee": true,
      "employeeNumber": "string",
      "firstName": "Ava",
      "groupHierarchy": "string",
      "groupId": 1,
      "groupName": "Ava Chen",
      "homePhoneNumber": {},
      "hourlyLaborRateCents": 1,
      "id": 1,
      "imagesCount": 1,
      "jobTitle": "string",
      "lastApiRequest": {},
      "lastMobileAppAccess": {},
      "lastName": "Chen",
      "lastWebAccess": {},
      "leaveDate": {},
      "licenseClass": {},
      "licenseNumber": {},
      "licenseState": {},
      "middleName": {},
      "mobilePhoneNumber": "string",
      "name": "Ava Chen",
      "otherPhoneNumber": {},
      "postalCode": {},
      "region": {},
      "startDate": "string",
      "streetAddress": {},
      "streetAddressLine2": {},
      "technician": true,
      "updatedAt": "string",
      "vehicleOperator": true,
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
| `birthDate` | object |  |
| `city` | object |  |
| `commentsCount` | number |  |
| `country` | object |  |
| `createdAt` | string |  |
| `defaultImageUrl` | string |  |
| `documentsCount` | number |  |
| `email` | object |  |
| `employee` | boolean |  |
| `employeeNumber` | string |  |
| `firstName` | string |  |
| `groupHierarchy` | string |  |
| `groupId` | number |  |
| `groupName` | string |  |
| `homePhoneNumber` | object |  |
| `hourlyLaborRateCents` | number |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `jobTitle` | string |  |
| `lastApiRequest` | object |  |
| `lastMobileAppAccess` | object |  |
| `lastName` | string |  |
| `lastWebAccess` | object |  |
| `leaveDate` | object |  |
| `licenseClass` | object |  |
| `licenseNumber` | object |  |
| `licenseState` | object |  |
| `middleName` | object |  |
| `mobilePhoneNumber` | string |  |
| `name` | string |  |
| `otherPhoneNumber` | object |  |
| `postalCode` | object |  |
| `region` | object |  |
| `startDate` | string |  |
| `streetAddress` | object |  |
| `streetAddressLine2` | object |  |
| `technician` | boolean |  |
| `updatedAt` | string |  |
| `vehicleOperator` | boolean |  |
| `workPhoneNumber` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET contacts` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

