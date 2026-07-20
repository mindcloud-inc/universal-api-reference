# Better Proposals: Get Quote Details

Retrieves quote details from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-quote-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-quote-details?connectionId=$CONNECTION_ID&quoteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "quoteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-quote-details?${params}`, {
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
| `quoteId` | string | yes | The Better Proposals quote ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "annualAmount": {},
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
      "monthlyAmount": {},
      "quarterlyAmount": {},
      "quoteAmount": {},
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
| `annualAmount` | object |  |
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
| `monthlyAmount` | object |  |
| `quarterlyAmount` | object |  |
| `quoteAmount` | object |  |
| `quoteTotal` | object |  |
| `status` | string |  |
| `vatAmount` | object |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /quote/:QUOTE_ID` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quote-details.md) for the provider-specific parameters and requirements.

