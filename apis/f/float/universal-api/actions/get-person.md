# Float: Get Person

Retrieves person details from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/get-person?connectionId=$CONNECTION_ID&peopleId=18636012" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "peopleId": "18636012"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/get-person?${params}`, {
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
| `peopleId` | number | yes | The person's id Example: `18636012`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "autoEmail": 1,
      "avatarFile": {},
      "contractor": 1,
      "costRate": {},
      "created": "string",
      "defaultHourlyRate": {},
      "department": {},
      "email": {},
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
      "startDate": {},
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
| `avatarFile` | object |  |
| `contractor` | number |  |
| `costRate` | object |  |
| `created` | string |  |
| `defaultHourlyRate` | object |  |
| `department` | object |  |
| `email` | object |  |
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
| `startDate` | object |  |
| `workDaysHours` | object |  |
| `workDaysHoursHistory` | object |  |

## Native endpoint

Through the native Float API, this operation is `GET /people/:people_id` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

