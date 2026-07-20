# Qualiobee: Update Learner

Updates an existing learner in Qualiobee.

```
PUT https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/update-learner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/update-learner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationUuid": "string",
  "learnerUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/update-learner', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationUuid": "string",
    "learnerUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationUuid` | string | yes |  |
| `learnerUuid` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `email` | string | no |  |
| `type` | string | no |  |
| `jobStatus` | string | no |  |
| `birthDate` | string | no |  |
| `birthCity` | string | no |  |
| `birthDepartment` | string | no |  |
| `needsAdaptation` | boolean | no |  |
| `phoneNumber` | string | no |  |
| `note` | string | no |  |
| `location.addressLine1` | string | no |  |
| `location.addressLine2` | string | no |  |
| `location.postCode` | string | no |  |
| `location.city` | string | no |  |
| `location.country` | string | no |  |

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

Through the native Qualiobee API, this operation is `PATCH /:organizationUuid/learner/:learnerUuid` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-learner.md) for the provider-specific parameters and requirements.

