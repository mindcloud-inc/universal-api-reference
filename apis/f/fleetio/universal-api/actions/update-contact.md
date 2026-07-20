# Fleetio: Update Contact

Updates an existing contact in Fleetio.

```
PUT https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The id of the relevant record |
| `firstName` | string | no | This Contact's first name. |
| `middleName` | string | no | This Contact's middle name. |
| `lastName` | string | no | This Contact's last name. |
| `birthDate` | date | no | This Contact's birth date. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `groupHierarchy` | string | no | If this Contact belongs to a [Group](/docs/api/groups), this will be a pipe delimited string representing the Group hierarchy. Each Group in the list is the parent of the `Groups` which follow. |
| `email` | string | no | This Contact's email address. |
| `mobilePhoneNumber` | string | no | This Contact's mobile phone number. |
| `homePhoneNumber` | string | no | This Contact's home phone number. |
| `workPhoneNumber` | string | no | This Contact's work phone number. |
| `otherPhoneNumber` | string | no | Any other phone number for this Contact. |
| `streetAddress` | string | no | The street address of this Contact. |
| `streetAddressLine2` | string | no | The second line of this Contact's street address. |
| `city` | string | no | The city of this Contact's address. |
| `region` | string | no | The region, state, province, or territory of this Contact's address. |
| `postalCode` | string | no | The postal code for this Contact's address. |
| `country` | string | no | The country where this Contact resides. |
| `employeeNumber` | string | no | This Contact's employee number. Must be unique. |
| `jobTitle` | string | no | This Contact's job title. |
| `startDate` | date | no | The date at which this Contact started, or is expected to start. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `leaveDate` | date | no | The date at which this Contact left, or is expected to leave. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `vehicleOperator` | boolean | no | Whether this Contact is a Vehicle Operator. |
| `licenseNumber` | string | no | The license number of this Contact. |
| `licenseClass` | string | no | The class of this Contact's license. |
| `licenseState` | string | no | The state, province, region, or territory of this Contact's license. |
| `hourlyLaborRate` | number | no | The hourly labor rate for this Contact. |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `groupId` | number | no |  |
| `licenseExpiration` | date | no | The date and time at which this Contact's license expires. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `employee` | boolean | no | Whether this Contact is an Employee. |
| `technician` | boolean | no | Whether this Contact is a Technician. |
| `userAccess` | boolean | no | Whether this Contact has User Access. This must be set to true if using `account_membership_attributes`. |
| `accountMembershipAttributes` | object | no | These attributes require an Organization Token or Partner Token to be present in the request. Any role or record set attributes will be ignored if `user_type` is `admin`. `admin_role_attributes` will be ignored if `user_type` is not `admin`. |
| `defaultImageAttributes` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partnerToken` | string | no |  |
| `organizationToken` | string | no |  |

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
      "defaultImageUrl": "https://example.com",
      "documentsCount": 1,
      "email": "ava@example.com",
      "employee": true,
      "employeeNumber": "string",
      "firstName": "Ava",
      "groupId": 1,
      "groupName": "Ava Chen",
      "homePhoneNumber": {},
      "hourlyLaborRate": {},
      "id": 1,
      "imagesCount": 1,
      "jobTitle": "string",
      "lastApiRequest": {},
      "lastMobileAppAccess": {},
      "lastName": "Chen",
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
      "startDate": "string",
      "streetAddress": {},
      "streetAddressLine2": {},
      "technician": true,
      "updatedAt": "string",
      "user": {},
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
| `archivedAt` | object |  |
| `birthDate` | object |  |
| `city` | object |  |
| `commentsCount` | number |  |
| `country` | object |  |
| `createdAt` | string |  |
| `defaultImageUrl` | string |  |
| `documentsCount` | number |  |
| `email` | string |  |
| `employee` | boolean |  |
| `employeeNumber` | string |  |
| `firstName` | string |  |
| `groupId` | number |  |
| `groupName` | string |  |
| `homePhoneNumber` | object |  |
| `hourlyLaborRate` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `jobTitle` | string |  |
| `lastApiRequest` | object |  |
| `lastMobileAppAccess` | object |  |
| `lastName` | string |  |
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
| `startDate` | string |  |
| `streetAddress` | object |  |
| `streetAddressLine2` | object |  |
| `technician` | boolean |  |
| `updatedAt` | string |  |
| `user` | object |  |
| `vehicleOperator` | boolean |  |
| `workPhoneNumber` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `PATCH contacts/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

