# DotCMS: Filter Users

Finds users in DotCMS by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/filter-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/filter-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/filter-users?${params}`, {
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
      "entity": [
        {
          "active": true,
          "actualCompanyId": "string",
          "admin": true,
          "backendUser": true,
          "birthday": {},
          "comments": {},
          "companyId": "string",
          "createDate": 1,
          "deleteDate": {},
          "deleteInProgress": true,
          "emailaddress": "ava@example.com",
          "emailAddress": "ava@example.com",
          "failedLoginAttempts": 1,
          "female": true,
          "firstName": "Ava",
          "frontendUser": true,
          "fullName": "Ava Chen",
          "gravitar": "string",
          "hasConsoleAccess": true,
          "id": "string",
          "languageId": "string",
          "lastLoginDate": 1,
          "lastLoginIP": "string",
          "lastName": "Chen",
          "male": true,
          "middleName": "Ava Chen",
          "modificationDate": 1,
          "name": "Ava Chen",
          "nickname": "Ava Chen",
          "passwordExpirationDate": {},
          "passwordExpired": true,
          "passwordReset": true,
          "timeZoneId": "string",
          "type": "string",
          "userId": "string"
        }
      ],
      "pagination": {
        "currentPage": 1,
        "perPage": 1,
        "totalEntries": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity[].active` | boolean |  |
| `entity[].actualCompanyId` | string |  |
| `entity[].admin` | boolean |  |
| `entity[].backendUser` | boolean |  |
| `entity[].birthday` | object |  |
| `entity[].comments` | object |  |
| `entity[].companyId` | string |  |
| `entity[].createDate` | number |  |
| `entity[].deleteDate` | object |  |
| `entity[].deleteInProgress` | boolean |  |
| `entity[].emailaddress` | string |  |
| `entity[].emailAddress` | string |  |
| `entity[].failedLoginAttempts` | number |  |
| `entity[].female` | boolean |  |
| `entity[].firstName` | string |  |
| `entity[].frontendUser` | boolean |  |
| `entity[].fullName` | string |  |
| `entity[].gravitar` | string |  |
| `entity[].hasConsoleAccess` | boolean |  |
| `entity[].id` | string |  |
| `entity[].languageId` | string |  |
| `entity[].lastLoginDate` | number |  |
| `entity[].lastLoginIP` | string |  |
| `entity[].lastName` | string |  |
| `entity[].male` | boolean |  |
| `entity[].middleName` | string |  |
| `entity[].modificationDate` | number |  |
| `entity[].name` | string |  |
| `entity[].nickname` | string |  |
| `entity[].passwordExpirationDate` | object |  |
| `entity[].passwordExpired` | boolean |  |
| `entity[].passwordReset` | boolean |  |
| `entity[].timeZoneId` | string |  |
| `entity[].type` | string |  |
| `entity[].userId` | string |  |
| `pagination.currentPage` | number |  |
| `pagination.perPage` | number |  |
| `pagination.totalEntries` | number |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/users/filter` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-users.md) for the provider-specific parameters and requirements.

