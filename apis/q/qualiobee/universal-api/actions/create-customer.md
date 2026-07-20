# Qualiobee: Create Customer

Creates a new customer in Qualiobee.

```
POST https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationUuid": "string",
  "name": "Ava Chen",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationUuid": "string",
    "name": "Ava Chen",
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationUuid` | string | yes | The Qualiobee organization UUID used in the request path |
| `name` | string | yes | The name of the company or the full name of the individual |
| `firstName` | string | yes | The first name of the referent in the company or the first name of the individual |
| `lastName` | string | yes | The last name of the referent in the company or the last name of the individual |
| `email` | string | yes | The email of the referent in the company or the email of the individual |
| `externalId` | string | no | Optional external identifier for the seeded customer |
| `phoneNumber` | string | no | The phone number of the referent in the company or the phone number of the individual |
| `siret` | string | no | The SIRET of the company |
| `naf` | string | no | The NAF code of the company |
| `note` | string | no | Some notes to save more details about the customer |
| `isIndividual` | boolean | no | Whether the customer is a company or an individual Default: `false`. |
| `isSoloLearner` | boolean | no | If true, creates a learner with the customer referent's data Default: `false`. |
| `location.addressLine1` | string | no | The first part of the address |
| `location.addressLine2` | string | no | The second part of the address |
| `location.postCode` | string | no | The postal code |
| `location.city` | string | no | The city |
| `location.country` | string | no | The country |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conventions": [
        {}
      ],
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deleteDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "isIndividual": true,
      "lastName": "Chen",
      "learners": {
        "creationDate": "2026-05-07T12:00:00.000Z",
        "deleteDate": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "externalId": "string",
        "firstName": "Ava",
        "jobStatus": "string",
        "lastName": "Chen",
        "needsAdaptation": true,
        "note": "string",
        "phoneNumber": "string",
        "type": "string",
        "updateDate": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "location": {
        "addressLine1": "string",
        "addressLine2": "string",
        "archiveDate": "2026-05-07T12:00:00.000Z",
        "city": "string",
        "country": "string",
        "creationDate": "2026-05-07T12:00:00.000Z",
        "postCode": "string",
        "updateDate": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "naf": "string",
      "name": "Ava Chen",
      "note": "string",
      "phoneNumber": "string",
      "siret": "string",
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
| `conventions` | array<object> | Related conventions for the customer when requested |
| `creationDate` | date | The date when the customer was created |
| `deleteDate` | date | The date when the customer was deleted |
| `email` | string | The email of the referent in the company or the email of the individual |
| `externalId` | string | The id of the customer in the external application (only for data importation) |
| `firstName` | string | The first name of the referent in the company or the first name of the individual |
| `isIndividual` | boolean | Whether the customer is a company or an individual |
| `lastName` | string | The last name of the referent in the company or the last name of the individual |
| `learners` | array<object> | Learners created or linked with the customer when returned by the API |
| `learners.creationDate` | date | The date when the learner was created |
| `learners.deleteDate` | date | The date when the learner was deleted |
| `learners.email` | string | The learner email |
| `learners.externalId` | string | The external identifier of the learner |
| `learners.firstName` | string | The learner first name |
| `learners.jobStatus` | string | The learner job status |
| `learners.lastName` | string | The learner last name |
| `learners.needsAdaptation` | boolean | Whether the learner needs adaptation support |
| `learners.note` | string | Additional notes saved on the learner |
| `learners.phoneNumber` | string | The learner phone number |
| `learners.type` | string | The learner type returned by Qualiobee |
| `learners.updateDate` | date | The last date when the learner was updated |
| `learners.uuid` | string | The uuid of the learner |
| `location` | object | The address of the company or the personnal address of the individual |
| `location.addressLine1` | string | The first line of the location address |
| `location.addressLine2` | string | The second line of the location address |
| `location.archiveDate` | date | The date when the location was archived |
| `location.city` | string | The city of the location |
| `location.country` | string | The country of the location |
| `location.creationDate` | date | The date when the location was created |
| `location.postCode` | string | The postal code of the location |
| `location.updateDate` | date | The last date when the location was updated |
| `location.uuid` | string | The uuid of the customer location |
| `naf` | string | The NAF code of the customer |
| `name` | string | The name of the company or the full name of the individual |
| `note` | string | A note that describe a bit more the customer |
| `phoneNumber` | string | The phone number of the referent in the company or the phone number of the individual |
| `siret` | string | The SIRET of the customer |
| `updateDate` | date | The last date when the customer was updated |
| `uuid` | string | The uuid of the customer |

## Native endpoint

Through the native Qualiobee API, this operation is `POST /:organizationUuid/customer` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

