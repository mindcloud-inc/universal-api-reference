# Deputy: Create Employee

Creates a new employee in Deputy.

```
POST https://connect.mindcloud.co/v1/universal/deputy/latest/actions/create-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deputy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/create-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.firstName": "Ava",
  "data.lastName": "Chen",
  "data.displayName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deputy/latest/actions/create-employee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.firstName": "Ava",
    "data.lastName": "Chen",
    "data.displayName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Employee payload object. |
| `data.firstName` | string | yes | The employee's given name. |
| `data.lastName` | string | yes | The employee's family name. |
| `data.displayName` | string | yes | The employee's display name. |
| `data.primaryLocation` | object | no | The employee's primary location object. |
| `data.primaryLocation.id` | number | no | The id of the employee's primary location. |
| `data.startDate` | date | no | The employee's start date. |
| `data.position` | string | no | The employee's position title. |
| `data.contact` | object | no | Employee contact object. |
| `data.contact.email1` | string | no | Primary work email address. |
| `data.contact.phone1` | string | no | Primary phone number. |
| `data.externalId` | string | no | An external identifier for the employee. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "allowAppraisal": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFieldData": [
        {}
      ],
      "displayName": "Ava Chen",
      "externalId": "string",
      "firstName": "Ava",
      "higherDuty": true,
      "history": "string",
      "id": "string",
      "lastName": "Chen",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "primaryLocation": {},
      "pronouns": {},
      "role": {},
      "startDate": "2026-05-07T12:00:00.000Z",
      "stressProfile": {},
      "trainingRecords": [
        {}
      ],
      "user": {},
      "workplaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `allowAppraisal` | boolean |  |
| `createdAt` | date |  |
| `customFieldData` | array<object> |  |
| `displayName` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `higherDuty` | boolean |  |
| `history` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `modifiedAt` | date |  |
| `primaryLocation` | object |  |
| `pronouns` | object |  |
| `role` | object |  |
| `startDate` | date |  |
| `stressProfile` | object |  |
| `trainingRecords` | array<object> |  |
| `user` | object |  |
| `workplaces` | array<object> |  |

## Native endpoint

Through the native Deputy API, this operation is `POST /api/management/v2/employees` (base URL `https://{{credentials.endpoint}}.deputy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employee.md) for the provider-specific parameters and requirements.

