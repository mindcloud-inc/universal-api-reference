# Better Proposals: Get Proposal Details

Retrieves proposal details from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-proposal-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-proposal-details?connectionId=$CONNECTION_ID&proposalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "proposalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-proposal-details?${params}`, {
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
| `proposalId` | string | yes | The Better Proposals proposal ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvedDate": "2026-05-07T12:00:00.000Z",
      "archived": "string",
      "brandID": "string",
      "companyCRMID": {},
      "companyID": "string",
      "coverHeadline": "string",
      "coverID": "string",
      "coverSubheader": "string",
      "customerJourneyID": {},
      "dateArchived": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateDeleted": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "dateMarkedDead": "2026-05-07T12:00:00.000Z",
      "dateSent": "2026-05-07T12:00:00.000Z",
      "deleted": "string",
      "description": {},
      "id": "string",
      "markDead": "string",
      "originalDateSent": "2026-05-07T12:00:00.000Z",
      "paid": "string",
      "personalMessage": {},
      "preview": "string",
      "proposalView": "string",
      "quoteID": "string",
      "signed": "string",
      "signedDate": "2026-05-07T12:00:00.000Z",
      "signedName": {},
      "signedTime": {},
      "subjectLine": {},
      "tax": "string",
      "taxAmount": {},
      "taxLabel": "string",
      "templateID": "string",
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
| `approvedDate` | date |  |
| `archived` | string |  |
| `brandID` | string |  |
| `companyCRMID` | object |  |
| `companyID` | string |  |
| `coverHeadline` | string |  |
| `coverID` | string |  |
| `coverSubheader` | string |  |
| `customerJourneyID` | object |  |
| `dateArchived` | date |  |
| `dateCreated` | date |  |
| `dateDeleted` | date |  |
| `dateEdited` | date |  |
| `dateMarkedDead` | date |  |
| `dateSent` | date |  |
| `deleted` | string |  |
| `description` | object |  |
| `id` | string |  |
| `markDead` | string |  |
| `originalDateSent` | date |  |
| `paid` | string |  |
| `personalMessage` | object |  |
| `preview` | string |  |
| `proposalView` | string |  |
| `quoteID` | string |  |
| `signed` | string |  |
| `signedDate` | date |  |
| `signedName` | object |  |
| `signedTime` | object |  |
| `subjectLine` | object |  |
| `tax` | string |  |
| `taxAmount` | object |  |
| `taxLabel` | string |  |
| `templateID` | string |  |
| `typeID` | string |  |
| `viewType` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /proposal/:PROPOSAL_ID` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-proposal-details.md) for the provider-specific parameters and requirements.

