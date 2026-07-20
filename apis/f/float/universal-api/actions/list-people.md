# Float: List People

Retrieves people from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-people?${params}`, {
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
      "active": 1,
      "autoEmail": 1,
      "avatarFile": "string",
      "contractor": 1,
      "costRate": {},
      "created": {},
      "defaultHourlyRate": {},
      "department": {},
      "email": "ava@example.com",
      "employeeType": 1,
      "endDate": {},
      "jobTitle": {},
      "modified": "string",
      "name": "Ava Chen",
      "nonWorkDays": {},
      "notes": {},
      "peopleId": 1,
      "peopleTypeId": 1,
      "regionId": 1,
      "roleId": {},
      "startDate": "string",
      "workDaysHours": {},
      "workDaysHoursHistory": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `autoEmail` | number |  |
| `avatarFile` | string |  |
| `contractor` | number |  |
| `costRate` | object |  |
| `created` | object |  |
| `defaultHourlyRate` | object |  |
| `department` | object |  |
| `email` | string |  |
| `employeeType` | number |  |
| `endDate` | object |  |
| `jobTitle` | object |  |
| `modified` | string |  |
| `name` | string |  |
| `nonWorkDays` | object |  |
| `notes` | object |  |
| `peopleId` | number |  |
| `peopleTypeId` | number |  |
| `regionId` | number |  |
| `roleId` | object |  |
| `startDate` | string |  |
| `workDaysHours` | object |  |
| `workDaysHoursHistory` | object |  |

## Native endpoint

Through the native Float API, this operation is `GET /people` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

