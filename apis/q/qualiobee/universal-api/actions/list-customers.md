# Qualiobee: List Customers

Retrieves customers from Qualiobee.

```
GET https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-customers?${params}`, {
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
| `organizationUuid` | string | yes | The Qualiobee organization UUID used in the request path |
| `relations` | list<string> | no | Related entities to include in each customer response Accepts multiple values as an array. |
| `uuid` | string | no | Filter customers by UUID |
| `externalId` | string | no | Filter customers by external ID |
| `name` | string | no | Filter customers by name |
| `firstName` | string | no | Filter customers by referent or individual first name |
| `lastName` | string | no | Filter customers by referent or individual last name |
| `email` | string | no | Filter customers by referent or individual email |
| `isIndividual` | string | no | Filter results to individual customers or companies |
| `withDeleted` | boolean | no | Include deleted customers in the results Default: `false`. |

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
      "learners": [
        {}
      ],
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
      "qualiobee": {
        "businessTitle": "string",
        "deleteDate": "2026-05-07T12:00:00.000Z",
        "organization": {
          "deleteDate": "2026-05-07T12:00:00.000Z",
          "uuid": "string"
        },
        "uuid": "string"
      },
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
| `learners` | array<object> | Related learners for the customer when requested |
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
| `qualiobee` | object | Qualiobee-specific metadata returned with the customer |
| `qualiobee.businessTitle` | string | The business title stored in Qualiobee |
| `qualiobee.deleteDate` | date | The date when the Qualiobee-specific customer record was deleted |
| `qualiobee.organization.deleteDate` | date | The date when the Qualiobee organization record was deleted |
| `qualiobee.organization.uuid` | string | The uuid of the Qualiobee organization that owns the customer |
| `qualiobee.uuid` | string | The uuid of the Qualiobee-specific customer record |
| `siret` | string | The SIRET of the customer |
| `updateDate` | date | The last date when the customer was updated |
| `uuid` | string | The uuid of the customer |

## Native endpoint

Through the native Qualiobee API, this operation is `GET /:organizationUuid/customer` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

