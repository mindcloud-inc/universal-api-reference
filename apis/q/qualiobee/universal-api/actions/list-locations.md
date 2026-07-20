# Qualiobee: List Locations

Retrieves locations from Qualiobee.

```
GET https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/list-locations?${params}`, {
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
| `withDeleted` | boolean | no | Default: `false`. |
| `relations` | list<string> | no | Accepts multiple values as an array. |
| `uuid` | string | no |  |
| `addressLine1` | string | no |  |
| `addressLine2` | string | no |  |
| `postCode` | string | no |  |
| `city` | string | no |  |
| `country` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressLine2": "string",
      "archiveDate": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "country": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "customer": {},
      "learner": {},
      "postCode": "string",
      "qualiobee": {
        "businessTitle": "string",
        "deleteDate": "2026-05-07T12:00:00.000Z",
        "organization": {
          "deleteDate": "2026-05-07T12:00:00.000Z",
          "uuid": "string"
        },
        "uuid": "string"
      },
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
| `addressLine1` | string | The first part of the address |
| `addressLine2` | string | The second part of the address |
| `archiveDate` | date | The date when the location was archived |
| `city` | string | The city |
| `country` | string | The country |
| `creationDate` | date | The date when the location was created |
| `customer` | object | The customer linked to this location when applicable |
| `learner` | object | The learner linked to this location when applicable |
| `postCode` | string | The postal code |
| `qualiobee` | object | Qualiobee-specific metadata returned with the location |
| `qualiobee.businessTitle` | string | The business title stored in Qualiobee |
| `qualiobee.deleteDate` | date | The date when the Qualiobee-specific location record was deleted |
| `qualiobee.organization` | object | The organization that owns the location record |
| `qualiobee.organization.deleteDate` | date | The date when the Qualiobee organization record was deleted |
| `qualiobee.organization.uuid` | string | The uuid of the Qualiobee organization that owns the location |
| `qualiobee.uuid` | string | The uuid of the Qualiobee-specific location record |
| `updateDate` | date | The last date when the location was updated |
| `uuid` | string | The uuid of the location |

## Native endpoint

Through the native Qualiobee API, this operation is `GET /:organizationUuid/location` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

