# PestPac: List Employees



```
GET https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PestPac `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/list-employees?${params}`, {
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
      "active": true,
      "address": "string",
      "addressLine2": "string",
      "birthDate": "string",
      "city": "Ava Chen",
      "companyWideAccessTemplate": "string",
      "defaultBranch": "string",
      "email": "ava@example.com",
      "employeeID": 1,
      "employeeNumber": "string",
      "firstName": "Ava",
      "hireDate": "string",
      "isTech": true,
      "isUser": true,
      "jobTitle": "string",
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "mobile": "string",
      "mobileAppModules": [
        "string"
      ],
      "mobileExtension": "string",
      "officePhone": "string",
      "officePhoneExtension": "string",
      "phone": "string",
      "phoneExtension": "string",
      "state": "string",
      "techID": 1,
      "terminationDate": "string",
      "timeZone": "string",
      "userDateFormat": "string",
      "userDefinedFields": [
        {}
      ],
      "userID": 1,
      "userLanguage": "string",
      "username": "Ava Chen",
      "useRouteOptimization": true,
      "verificationStatus": "string",
      "workWaveAccount": "string",
      "workWaveID": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `address` | string |  |
| `addressLine2` | string |  |
| `birthDate` | string |  |
| `city` | string |  |
| `companyWideAccessTemplate` | string |  |
| `defaultBranch` | string |  |
| `email` | string |  |
| `employeeID` | number |  |
| `employeeNumber` | string |  |
| `firstName` | string |  |
| `hireDate` | string |  |
| `isTech` | boolean |  |
| `isUser` | boolean |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `middleName` | string |  |
| `mobile` | string |  |
| `mobileAppModules` | array<string> |  |
| `mobileExtension` | string |  |
| `officePhone` | string |  |
| `officePhoneExtension` | string |  |
| `phone` | string |  |
| `phoneExtension` | string |  |
| `state` | string |  |
| `techID` | number |  |
| `terminationDate` | string |  |
| `timeZone` | string |  |
| `userDateFormat` | string |  |
| `userDefinedFields` | array<object> |  |
| `userID` | number |  |
| `userLanguage` | string |  |
| `username` | string |  |
| `useRouteOptimization` | boolean |  |
| `verificationStatus` | string |  |
| `workWaveAccount` | string |  |
| `workWaveID` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native PestPac API, this operation is `GET lookups/Employees` (base URL `https://api.workwave.com/pestpac/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

