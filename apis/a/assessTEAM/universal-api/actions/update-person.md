# AssessTEAM: Update Person

Updates an existing person in AssessTEAM.

```
PUT https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/update-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssessTEAM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/update-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "personCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/update-person', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "personCode": "string"
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
| `dateOfJoining` | string | no | Date of joining, for example 2026-04-07. |
| `email` | string | no | Email address, for example sample1@yourcompany.com. |
| `contactNumber` | string | no | Contact number, for example 1234567890. |
| `userPermissions` | string | no | User permission or role, for example Employee. |
| `team` | string | no | Team assigned to person, for example Administration. |
| `jobTitle` | string | no | Job title, for example QA Analyst. |
| `evaluators` | string | no | Person evaluator names, for example Jack Doe. |
| `enableSelfEvaluation` | boolean | no | Enable self evaluation. |

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

Through the native AssessTEAM API, this operation is `POST /person/updateperson` (base URL `https://restapi.assessteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person.md) for the provider-specific parameters and requirements.

