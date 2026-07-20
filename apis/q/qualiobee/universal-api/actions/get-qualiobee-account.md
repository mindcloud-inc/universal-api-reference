# Qualiobee: Get Qualiobee Account

Retrieves a Qualiobee account by UUID.

```
GET https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-qualiobee-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-qualiobee-account?connectionId=$CONNECTION_ID&organizationUuid=string&qualiobeeUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationUuid": "string",
  "qualiobeeUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/get-qualiobee-account?${params}`, {
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
| `qualiobeeUuid` | string | yes |  |
| `withDeleted` | boolean | no | Default: `false`. |
| `relations` | list<string> | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {},
      "billingEmailAddress": "ava@example.com",
      "businessTitle": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deleteDate": "2026-05-07T12:00:00.000Z",
      "headquarter": {},
      "naf": "string",
      "organization": {
        "creationDate": "2026-05-07T12:00:00.000Z",
        "deleteDate": "2026-05-07T12:00:00.000Z",
        "title": "string",
        "updateDate": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "qualiopiCertifNum": "string",
      "rcs": "string",
      "recommandation": 1,
      "registrationNumber": "string",
      "registrationRegion": "string",
      "satisfaction": 1,
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
| `billingAddress` | object | The billing address of the organization |
| `billingEmailAddress` | string | The billing email address of the organization |
| `businessTitle` | string | The business title of your organization |
| `creationDate` | date | The date when the Qualiobee account was created |
| `deleteDate` | date | The date when the Qualiobee account was deleted |
| `headquarter` | object | The headquarter location of the organization |
| `naf` | string | The NAF code of your organization |
| `organization` | object | The organization record linked to this Qualiobee account |
| `organization.creationDate` | date | The date when the linked organization was created |
| `organization.deleteDate` | date | The date when the linked organization was deleted |
| `organization.title` | string | The title of the linked organization |
| `organization.updateDate` | date | The last date when the linked organization was updated |
| `organization.uuid` | string | The uuid of the linked organization |
| `qualiopiCertifNum` | string | The Qualiopi certificate number of your organization |
| `rcs` | string | The RCS of your organization |
| `recommandation` | number | The recommendation rate of your organization |
| `registrationNumber` | string | The registration number of your organization |
| `registrationRegion` | string | The region where your organization is registered |
| `satisfaction` | number | The satisfaction rate of your organization |
| `siret` | string | The SIRET of your organization |
| `updateDate` | date | The last date when the Qualiobee account was updated |
| `uuid` | string | The uuid of the Qualiobee account |

## Native endpoint

Through the native Qualiobee API, this operation is `GET /:organizationUuid/qualiobee/:qualiobeeUuid` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qualiobee-account.md) for the provider-specific parameters and requirements.

