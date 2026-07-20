# Better Proposals: Create Proposal

Creates a proposal in Better Proposals.

```
POST https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-proposal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-proposal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-proposal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | yes | Either a company ID or company name. When a name is provided, Better Proposals creates the company if needed. |
| `cover` | string | no | Cover ID. |
| `template` | string | no | Template ID. When provided, Better Proposals copies the template into the new proposal. |
| `documentType` | string | no | Document type ID or name. If omitted, Better Proposals uses the default proposal document type. |
| `brand` | string | no | Brand ID. If omitted, Better Proposals uses the default brand. |
| `currency` | string | no | Currency code in 3-letter format, for example USD. |
| `tax` | boolean | no | Whether to apply tax. If omitted, Better Proposals uses the default brand setting. |
| `taxLabel` | string | no | Tax label. If omitted, Better Proposals uses the default brand setting. |
| `taxAmount` | number | no | Tax amount. If omitted, Better Proposals uses the default brand setting. |
| `contacts[]` | array<object> | no | Array of contact objects with FirstName, Surname, Email, and Signature fields. |
| `mergeTags[]` | array<object> | no | Array of custom merge-tag objects with tag and value fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brandID": "string",
      "companyCRMID": {},
      "companyID": "string",
      "coverHeadline": "string",
      "coverID": "string",
      "coverSubheader": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "description": {},
      "id": "string",
      "preview": "string",
      "proposalView": "string",
      "taxAmount": {},
      "taxLabel": "string",
      "templateID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandID` | string |  |
| `companyCRMID` | object |  |
| `companyID` | string |  |
| `coverHeadline` | string |  |
| `coverID` | string |  |
| `coverSubheader` | string |  |
| `dateCreated` | date |  |
| `description` | object |  |
| `id` | string |  |
| `preview` | string |  |
| `proposalView` | string |  |
| `taxAmount` | object |  |
| `taxLabel` | string |  |
| `templateID` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `POST /proposal/create` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-proposal.md) for the provider-specific parameters and requirements.

