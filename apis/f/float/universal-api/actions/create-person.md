# Float: Create Person

Creates a new person in Float.

```
POST https://connect.mindcloud.co/v1/universal/float/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/float/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Jordan Rivera"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Jordan Rivera"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The person's full name Example: `Jordan Rivera`. |

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
      "tags": {},
      "workDayHours": {},
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
| `tags` | object |  |
| `workDayHours` | object |  |
| `workDaysHours` | object |  |
| `workDaysHoursHistory` | object |  |

## Native endpoint

Through the native Float API, this operation is `POST /people` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

