# Qualiobee: Get Customer

Retrieves a customer from Qualiobee.

```
GET https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-customer?connectionId=$CONNECTION_ID&organizationUuid=string&customerUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationUuid": "string",
  "customerUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-customer?${params}`, {
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
| `customerUuid` | string | yes | The uuid of the customer to fetch |
| `relations` | list<string> | no | Related entities to include in the customer response Accepts multiple values as an array. |
| `withDeleted` | boolean | no | Include deleted customer data in the response Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deleteDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "isIndividual": true,
      "lastName": "Chen",
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
| `creationDate` | date |  |
| `deleteDate` | date |  |
| `email` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `isIndividual` | boolean |  |
| `lastName` | string |  |
| `location` | object |  |
| `location.addressLine1` | string |  |
| `location.addressLine2` | string |  |
| `location.archiveDate` | date |  |
| `location.city` | string |  |
| `location.country` | string |  |
| `location.creationDate` | date |  |
| `location.postCode` | string |  |
| `location.updateDate` | date |  |
| `location.uuid` | string |  |
| `naf` | string |  |
| `name` | string |  |
| `note` | string |  |
| `phoneNumber` | string |  |
| `siret` | string |  |
| `updateDate` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Qualiobee API, this operation is `GET /:organizationUuid/customer/:customerUuid` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

