# Qualiobee: Update Customer

Updates an existing customer in Qualiobee.

```
PUT https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationUuid": "string",
  "customerUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationUuid": "string",
    "customerUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationUuid` | string | yes |  |
| `customerUuid` | string | yes |  |
| `name` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `email` | string | no |  |
| `phoneNumber` | string | no |  |
| `siret` | string | no |  |
| `naf` | string | no |  |
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

Through the native Qualiobee API, this operation is `PATCH /:organizationUuid/customer/:customerUuid` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

