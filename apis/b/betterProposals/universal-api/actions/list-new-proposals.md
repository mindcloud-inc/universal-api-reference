# Better Proposals: List New Proposals

Retrieves new proposals from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-new-proposals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-new-proposals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-new-proposals?${params}`, {
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
| `page` | number | no | Page number. Default: 1. Default: `1`. |
| `perPage` | number | no | Results per page. Default: 10. Default: `10`. |
| `documentTypeId` | string | no | DocumentTypeID for filtering. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annualTotal": {},
      "brandID": "string",
      "companyCRMID": {},
      "companyName": "Ava Chen",
      "coverID": "string",
      "cRMOpportunityID": {},
      "currencyCode": "string",
      "currencyName": "Ava Chen",
      "currencySymbol": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "description": {},
      "id": "string",
      "monthlyTotal": {},
      "oneOffTotal": {},
      "preview": "string",
      "proposalView": "string",
      "quarterlyTotal": {},
      "quoteID": "string",
      "taxName": "Ava Chen",
      "taxPercentage": {},
      "typeID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annualTotal` | object |  |
| `brandID` | string |  |
| `companyCRMID` | object |  |
| `companyName` | string |  |
| `coverID` | string |  |
| `cRMOpportunityID` | object |  |
| `currencyCode` | string |  |
| `currencyName` | string |  |
| `currencySymbol` | string |  |
| `dateCreated` | date |  |
| `description` | object |  |
| `id` | string |  |
| `monthlyTotal` | object |  |
| `oneOffTotal` | object |  |
| `preview` | string |  |
| `proposalView` | string |  |
| `quarterlyTotal` | object |  |
| `quoteID` | string |  |
| `taxName` | string |  |
| `taxPercentage` | object |  |
| `typeID` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /proposal/new` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-new-proposals.md) for the provider-specific parameters and requirements.

