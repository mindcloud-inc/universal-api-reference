# AssessTEAM: Add Person

Creates a new person in AssessTEAM.

```
POST https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/add-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssessTEAM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/add-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "personCode": "string",
  "dateOfJoining": "string",
  "email": "ava@example.com",
  "contactNumber": "string",
  "team": "string",
  "jobTitle": "string",
  "enableSelfEvaluation": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/add-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "personCode": "string",
    "dateOfJoining": "string",
    "email": "ava@example.com",
    "contactNumber": "string",
    "team": "string",
    "jobTitle": "string",
    "enableSelfEvaluation": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Person first name, for example Jon. |
| `lastName` | string | yes | Person last name, for example Doe. |
| `personCode` | string | yes | Unique person code, for example 1001. |
| `dateOfJoining` | string | yes | Date of joining, for example 2026-04-07. |
| `email` | string | yes | Email address, for example sample1@yourcompany.com. |
| `contactNumber` | string | yes | Contact number, for example 1234567890. |
| `userPermissions` | string | no | User permission or role, for example Employee. |
| `team` | string | yes | Team assigned to person, for example Administration. |
| `jobTitle` | string | yes | Job title, for example QA Analyst. |
| `evaluators` | string | no | Person evaluator names, for example Jack Doe. |
| `enableSelfEvaluation` | boolean | yes | Enable self evaluation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "data": {},
        "message": "string",
        "personID": 1,
        "statusCode": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.data` | object |  |
| `result.message` | string |  |
| `result.personID` | number |  |
| `result.statusCode` | number |  |

## Native endpoint

Through the native AssessTEAM API, this operation is `POST /person/addperson` (base URL `https://restapi.assessteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-person.md) for the provider-specific parameters and requirements.

