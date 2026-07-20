# Qualiobee: Create Formation

Creates a new formation in Qualiobee.

```
POST https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-formation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qualiobee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-formation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qualiobee/latest/actions/create-formation', {
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
| `title` | string | no |  |
| `externalId` | string | no |  |
| `description` | string | no |  |
| `pedagogiqueMethode` | string | no |  |
| `prerequisites` | string | no |  |
| `audience` | string | no |  |
| `evaluationMethode` | string | no |  |
| `actionMethode` | string | no |  |
| `usingBeehelp` | boolean | no | Default: `false`. |
| `usingSignature` | boolean | no | Default: `false`. |
| `usingSignatureMedia` | boolean | no | Default: `true`. |
| `subtractType` | string | no |  |
| `specialtyCode` | string | no |  |
| `certifType` | string | no | Default: `NONE`. |
| `certifLevel` | string | no | Default: `RCP0`. |
| `pricing.strategy` | string | no | Default: `BY_HOUR`. |
| `pricing.precision` | string | no | Default: `FIXED`. |
| `pricing.moneyValue` | number | no | Default: `0`. |
| `pricing.taxRate` | number | no | Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archiveDate": "2026-05-07T12:00:00.000Z",
      "certifLevel": "string",
      "certifType": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "externalId": "string",
      "pricing": {
        "computedBaseTotal": 1,
        "computedTotal": 1,
        "computedTTCTotal": 1,
        "creationDate": "2026-05-07T12:00:00.000Z",
        "daysCount": 1,
        "deleteDate": "2026-05-07T12:00:00.000Z",
        "hoursCount": 1,
        "moneyValue": 1,
        "name": "Ava Chen",
        "precision": "string",
        "scope": "string",
        "strategy": "string",
        "taxRate": 1,
        "updateDate": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      },
      "qualiobee": {
        "businessTitle": "string",
        "deleteDate": "2026-05-07T12:00:00.000Z",
        "organization": {
          "deleteDate": "2026-05-07T12:00:00.000Z",
          "uuid": "string"
        },
        "uuid": "string"
      },
      "specialtyCode": "string",
      "state": "string",
      "subtractType": "string",
      "title": "string",
      "updateDate": "2026-05-07T12:00:00.000Z",
      "usingBeehelp": true,
      "usingSignature": true,
      "usingSignatureMedia": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archiveDate` | date | The date when the formation was archived |
| `certifLevel` | string | The certification level configured for the formation |
| `certifType` | string | The certification type configured for the formation |
| `creationDate` | date | The date when the formation was created |
| `description` | string | The formation description |
| `externalId` | string | The external identifier of the formation |
| `pricing` | object | Pricing information for the formation |
| `pricing.computedBaseTotal` | number | The computed base total |
| `pricing.computedTotal` | number | The computed total |
| `pricing.computedTTCTotal` | number | The computed TTC total |
| `pricing.creationDate` | date | The date when the pricing record was created |
| `pricing.daysCount` | number | The number of days captured in pricing |
| `pricing.deleteDate` | date | The date when the pricing record was deleted |
| `pricing.hoursCount` | number | The number of hours captured in pricing |
| `pricing.moneyValue` | number | The net price value |
| `pricing.name` | string | The pricing label |
| `pricing.precision` | string | The pricing precision |
| `pricing.scope` | string | The pricing scope |
| `pricing.strategy` | string | The pricing strategy |
| `pricing.taxRate` | number | The applied tax rate |
| `pricing.updateDate` | date | The last date when the pricing record was updated |
| `pricing.uuid` | string | The uuid of the pricing record |
| `qualiobee` | object | The linked Qualiobee account |
| `qualiobee.businessTitle` | string | The business title of the linked Qualiobee account |
| `qualiobee.deleteDate` | date | The delete date of the linked Qualiobee account |
| `qualiobee.organization` | object | The linked organization |
| `qualiobee.organization.deleteDate` | date | The delete date of the linked organization |
| `qualiobee.organization.uuid` | string | The uuid of the linked organization |
| `qualiobee.uuid` | string | The uuid of the linked Qualiobee account |
| `specialtyCode` | string | The specialty code configured for the formation |
| `state` | string | The current state of the formation |
| `subtractType` | string | The subtract type configured for the formation |
| `title` | string | The formation title |
| `updateDate` | date | The last date when the formation was updated |
| `usingBeehelp` | boolean | Whether Beehelp is enabled for the formation |
| `usingSignature` | boolean | Whether signature is enabled for the formation |
| `usingSignatureMedia` | boolean | Whether signature media is enabled for the formation |
| `uuid` | string | The uuid of the formation |

## Native endpoint

Through the native Qualiobee API, this operation is `POST /:organizationUuid/formation` (base URL `https://app.qualiobee.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-formation.md) for the provider-specific parameters and requirements.

