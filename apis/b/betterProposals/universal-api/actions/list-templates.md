# Better Proposals: List Templates

Retrieves all templates from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-templates?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "annualAmount": {},
      "brandID": "string",
      "categoryID": {},
      "coverID": {},
      "createdBy": "string",
      "customerJourneyID": {},
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "default": "string",
      "deleted": "string",
      "description": {},
      "editedBy": {},
      "fromMarketplace": "string",
      "id": "string",
      "industryID": {},
      "monthlyAmount": {},
      "quarterlyAmount": {},
      "quoteAmount": {},
      "sampleTemplate": "string",
      "templateName": "Ava Chen",
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
| `accountID` | string |  |
| `annualAmount` | object |  |
| `brandID` | string |  |
| `categoryID` | object |  |
| `coverID` | object |  |
| `createdBy` | string |  |
| `customerJourneyID` | object |  |
| `dateCreated` | date |  |
| `dateEdited` | date |  |
| `default` | string |  |
| `deleted` | string |  |
| `description` | object |  |
| `editedBy` | object |  |
| `fromMarketplace` | string |  |
| `id` | string |  |
| `industryID` | object |  |
| `monthlyAmount` | object |  |
| `quarterlyAmount` | object |  |
| `quoteAmount` | object |  |
| `sampleTemplate` | string |  |
| `templateName` | string |  |
| `typeID` | string |  |
| `viewType` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /template` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

