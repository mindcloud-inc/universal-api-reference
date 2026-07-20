# AssessTEAM: Get Person

Retrieves a person by person code from AssessTEAM.

```
GET https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssessTEAM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/get-person?connectionId=$CONNECTION_ID&personCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/get-person?${params}`, {
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
| `personCode` | string | yes | Unique person code, for example 1001. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contactnumber": "string",
        "dateofjoining": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "evaluators": {},
        "firstname": "Ava",
        "jobtitle": "string",
        "lastname": "Chen",
        "personcode": "string",
        "team": "string",
        "userpermissions": {}
      },
      "message": "string",
      "personID": 1,
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.contactnumber` | string |  |
| `data.dateofjoining` | date |  |
| `data.email` | string |  |
| `data.evaluators` | object |  |
| `data.firstname` | string |  |
| `data.jobtitle` | string |  |
| `data.lastname` | string |  |
| `data.personcode` | string |  |
| `data.team` | string |  |
| `data.userpermissions` | object |  |
| `message` | string |  |
| `personID` | number |  |
| `statusCode` | number |  |

## Native endpoint

Through the native AssessTEAM API, this operation is `POST /person/getperson` (base URL `https://restapi.assessteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

