# Aspire: List Employee Incidents



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-employee-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-employee-incidents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-employee-incidents?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "branchID": 1,
      "branchName": "Ava Chen",
      "companyID": 1,
      "companyName": "Ava Chen",
      "contactID": 1,
      "contactTypeID": 1,
      "contactTypeName": "Ava Chen",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "defaultWorkersCompID": 1,
      "defaultWorkersCompName": "Ava Chen",
      "defaultWorkersCompStateProvinceCode": "string",
      "email": "ava@example.com",
      "employeeNumber": "string",
      "employeePin": "string",
      "fax": "string",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "homeAddress": {
        "addressID": 1,
        "createdByUserId": 1,
        "createdByUserName": "Ava Chen",
        "createdOn": "2026-05-07T12:00:00.000Z"
      },
      "homePhone": "string",
      "lastModifiedByUserId": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastName": "Chen",
      "mobilePhone": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "officeAddress": {
        "addressID": 1,
        "addressLine1": "string",
        "city": "Ava Chen",
        "createdByUserId": 1,
        "createdByUserName": "Ava Chen",
        "createdOn": "2026-05-07T12:00:00.000Z",
        "stateProvinceCode": "string",
        "zipCode": "string"
      },
      "officePhone": "string",
      "payScheduleID": 1,
      "prospectRating": "string",
      "prospectRatingName": "Ava Chen",
      "salutation": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `companyID` | number |  |
| `companyName` | string |  |
| `contactID` | number |  |
| `contactTypeID` | number |  |
| `contactTypeName` | string |  |
| `createdDateTime` | date |  |
| `defaultWorkersCompID` | number |  |
| `defaultWorkersCompName` | string |  |
| `defaultWorkersCompStateProvinceCode` | string |  |
| `email` | string |  |
| `employeeNumber` | string |  |
| `employeePin` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `homeAddress.addressID` | number |  |
| `homeAddress.createdByUserId` | number |  |
| `homeAddress.createdByUserName` | string |  |
| `homeAddress.createdOn` | date |  |
| `homePhone` | string |  |
| `lastModifiedByUserId` | number |  |
| `lastModifiedByUserName` | string |  |
| `lastName` | string |  |
| `mobilePhone` | string |  |
| `modifiedDate` | date |  |
| `notes` | string |  |
| `officeAddress.addressID` | number |  |
| `officeAddress.addressLine1` | string |  |
| `officeAddress.city` | string |  |
| `officeAddress.createdByUserId` | number |  |
| `officeAddress.createdByUserName` | string |  |
| `officeAddress.createdOn` | date |  |
| `officeAddress.stateProvinceCode` | string |  |
| `officeAddress.zipCode` | string |  |
| `officePhone` | string |  |
| `payScheduleID` | number |  |
| `prospectRating` | string |  |
| `prospectRatingName` | string |  |
| `salutation` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET EmployeeIncidents` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employee-incidents.md) for the provider-specific parameters and requirements.

