# Qualiobee: Create Location

Creates a new location in Qualiobee.

```
POST https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationUuid` | string | yes |  |
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

Through the native Qualiobee API, this operation is `POST /:organizationUuid/location` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

