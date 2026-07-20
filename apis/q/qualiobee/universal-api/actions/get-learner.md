# Qualiobee: Get Learner

Retrieves a learner from Qualiobee.

```
GET https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-learner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-learner?connectionId=$CONNECTION_ID&organizationUuid=string&learnerUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationUuid": "string",
  "learnerUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-learner?${params}`, {
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
| `organizationUuid` | string | yes |  |
| `learnerUuid` | string | yes |  |
| `withDeleted` | boolean | no | Default: `false`. |
| `relations` | list<string> | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthCity": "string",
      "birthDate": "2026-05-07T12:00:00.000Z",
      "birthDepartment": "string",
      "convocations": [
        {}
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "customer": {},
      "deleteDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "jobStatus": "string",
      "lastName": "Chen",
      "location": {},
      "needsAdaptation": true,
      "note": "string",
      "phoneNumber": "string",
      "type": "string",
      "updateDate": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthCity` | string | The birth city of the learner |
| `birthDate` | date | The birth date of the learner |
| `birthDepartment` | string | The birth department of the learner |
| `convocations` | array<object> | Related convocations for the learner when requested |
| `creationDate` | date | The date when the learner was created |
| `customer` | object | The customer linked to the learner |
| `deleteDate` | date | The date when the learner was deleted |
| `email` | string | The email of the learner |
| `externalId` | string | The id of the learner in the external application (only for data importation) |
| `firstName` | string | The first name of the learner |
| `jobStatus` | string | Extra job-status details when the learner type is OTHER |
| `lastName` | string | The last name of the learner |
| `location` | object | The personal address of the learner |
| `needsAdaptation` | boolean | Whether the learner needs some kind of adaptation |
| `note` | string | A note that describes the learner |
| `phoneNumber` | string | The phone number of the learner |
| `type` | string | The type of the learner |
| `updateDate` | date | The last date when the learner was updated |
| `uuid` | string | The uuid of the learner |

## Native endpoint

Through the native Qualiobee API, this operation is `GET /:organizationUuid/learner/:learnerUuid` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-learner.md) for the provider-specific parameters and requirements.

