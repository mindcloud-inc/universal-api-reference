# Encircle: Create Property Claim

Creates a property claim in Encircle.

```
POST https://connect.mindcloud.co/v1/universal/encircle/latest/actions/create-property-claim
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encircle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/create-property-claim" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "brandId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encircle/latest/actions/create-property-claim', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "brandId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes |  |
| `brandId` | number | yes |  |
| `dateOfLoss` | date | no |  |
| `fullAddress` | string | no |  |
| `insurerIdentifier` | string | no |  |
| `policyholderName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `typeOfLoss` | string | no |  |
| `locale` | list | no | One of: `en`, `es`, `fr`. |
| `adjusterName` | string | no |  |
| `assignmentIdentifier` | string | no |  |
| `catCode` | string | no |  |
| `contentsEstimate` | number | no |  |
| `contractorIdentifier` | string | no |  |
| `dateClaimCreated` | date | no |  |
| `defaultDepreciation` | number | no |  |
| `emergencyEstimate` | number | no |  |
| `lossDetails` | string | no |  |
| `maxDepreciation` | number | no |  |
| `policyholderEmailAddress` | string | no |  |
| `policyholderPhoneNumber` | string | no |  |
| `projectManagerName` | string | no |  |
| `repairEstimate` | number | no |  |
| `salesTax` | number | no |  |
| `brokerOrAgentName` | string | no |  |
| `insuranceCompanyName` | string | no |  |
| `policyNumber` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Encircle API returns.

## Native endpoint

Through the native Encircle API, this operation is `POST /v1/property_claims` (base URL `https://api.encircleapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-property-claim.md) for the provider-specific parameters and requirements.

