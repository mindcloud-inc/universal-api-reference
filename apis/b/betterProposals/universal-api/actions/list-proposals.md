# Better Proposals: List Proposals

Retrieves all proposals from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-proposals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-proposals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-proposals?${params}`, {
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
      "amount": "string",
      "amountDesc": {},
      "annualTotal": {},
      "assignedTo": "string",
      "brandID": "string",
      "companyCRMID": {},
      "companyName": "Ava Chen",
      "contacts": [
        {
          "email": "ava@example.com",
          "firstName": "Ava",
          "link": "https://example.com",
          "surname": "Ava Chen"
        }
      ],
      "coverID": "string",
      "cRMOpportunityID": {},
      "currencyCode": "string",
      "currencyName": "Ava Chen",
      "currencySymbol": "string",
      "customerJourneyID": {},
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "datePaid": "2026-05-07T12:00:00.000Z",
      "dateSent": "2026-05-07T12:00:00.000Z",
      "description": {},
      "editLock": {},
      "id": "string",
      "monthlyTotal": {},
      "oneOffTotal": {},
      "originalDateSent": "2026-05-07T12:00:00.000Z",
      "paid": "string",
      "personalMessage": {},
      "preview": "string",
      "proposalPassword": {},
      "proposalView": "string",
      "quarterlyTotal": {},
      "quoteID": "string",
      "signed": "string",
      "signedDate": "2026-05-07T12:00:00.000Z",
      "signedEmail": {},
      "signedFirstName": {},
      "signedName": {},
      "signedSurname": {},
      "signedTime": {},
      "signOrder": "string",
      "subjectLine": {},
      "tax": "string",
      "taxAmount": {},
      "taxLabel": "string",
      "typeID": "string",
      "viewType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `amountDesc` | object |  |
| `annualTotal` | object |  |
| `assignedTo` | string |  |
| `brandID` | string |  |
| `companyCRMID` | object |  |
| `companyName` | string |  |
| `contacts[].email` | string |  |
| `contacts[].firstName` | string |  |
| `contacts[].link` | string |  |
| `contacts[].surname` | string |  |
| `coverID` | string |  |
| `cRMOpportunityID` | object |  |
| `currencyCode` | string |  |
| `currencyName` | string |  |
| `currencySymbol` | string |  |
| `customerJourneyID` | object |  |
| `dateCreated` | date |  |
| `datePaid` | date |  |
| `dateSent` | date |  |
| `description` | object |  |
| `editLock` | object |  |
| `id` | string |  |
| `monthlyTotal` | object |  |
| `oneOffTotal` | object |  |
| `originalDateSent` | date |  |
| `paid` | string |  |
| `personalMessage` | object |  |
| `preview` | string |  |
| `proposalPassword` | object |  |
| `proposalView` | string |  |
| `quarterlyTotal` | object |  |
| `quoteID` | string |  |
| `signed` | string |  |
| `signedDate` | date |  |
| `signedEmail` | object |  |
| `signedFirstName` | object |  |
| `signedName` | object |  |
| `signedSurname` | object |  |
| `signedTime` | object |  |
| `signOrder` | string |  |
| `subjectLine` | object |  |
| `tax` | string |  |
| `taxAmount` | object |  |
| `taxLabel` | string |  |
| `typeID` | string |  |
| `viewType` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /proposal` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-proposals.md) for the provider-specific parameters and requirements.

