# MILKEE: Update Proposal

Updates an existing proposal in MILKEE.

```
PUT https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-proposal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-proposal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "4640",
  "proposalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/update-proposal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "4640",
    "proposalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |
| `customerId` | number | no | Customer ID for the proposal. |
| `discountRate` | number | no | Overall discount percentage. |
| `positions` | string | no | Proposal positions as a JSON string. |
| `projectId` | number | no | Associated project ID. |
| `proposalId` | string | yes | The numeric MILKEE proposal ID used in the request path. |
| `remarks` | string | no | Bottom remarks. |
| `signatureRemark` | string | no | Text shown in the signature area. |
| `taxRateId` | number | no | Tax rate ID. |
| `title` | string | no | Proposal title. |
| `validUntil` | string | no | Proposal expiration date. |
| `withSignature` | boolean | no | Show a signature area on the proposal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native MILKEE API, this operation is `PUT /companies/:companyId/proposals/:proposalId` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-proposal.md) for the provider-specific parameters and requirements.

