# Better Proposals: List Quotes

Retrieves all quotes from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-quotes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/list-quotes?${params}`, {
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
      "annualAmount": "string",
      "archived": "string",
      "archivedBy": {},
      "companyID": "string",
      "createdBy": "string",
      "dateAccepted": "2026-05-07T12:00:00.000Z",
      "dateArchived": "2026-05-07T12:00:00.000Z",
      "dateCompleted": "2026-05-07T12:00:00.000Z",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateDeleted": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "dateMarkedDead": "2026-05-07T12:00:00.000Z",
      "deleted": "string",
      "deletedBy": {},
      "editedBy": "string",
      "id": "string",
      "markDead": "string",
      "markedDeadBy": {},
      "monthlyAmount": "string",
      "quarterlyAmount": "string",
      "quoteAmount": "string",
      "quoteTotal": {},
      "status": "string",
      "vatAmount": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `annualAmount` | string |  |
| `archived` | string |  |
| `archivedBy` | object |  |
| `companyID` | string |  |
| `createdBy` | string |  |
| `dateAccepted` | date |  |
| `dateArchived` | date |  |
| `dateCompleted` | date |  |
| `dateCreated` | date |  |
| `dateDeleted` | date |  |
| `dateEdited` | date |  |
| `dateMarkedDead` | date |  |
| `deleted` | string |  |
| `deletedBy` | object |  |
| `editedBy` | string |  |
| `id` | string |  |
| `markDead` | string |  |
| `markedDeadBy` | object |  |
| `monthlyAmount` | string |  |
| `quarterlyAmount` | string |  |
| `quoteAmount` | string |  |
| `quoteTotal` | object |  |
| `status` | string |  |
| `vatAmount` | object |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /quote` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-quotes.md) for the provider-specific parameters and requirements.

