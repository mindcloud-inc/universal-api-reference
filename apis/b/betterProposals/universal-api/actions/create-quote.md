# Better Proposals: Create Quote

Creates a quote in Better Proposals.

```
POST https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | Company ID. |
| `templateId` | string | no | Template ID. If provided, Better Proposals retrieves the amount from the template. |

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

Through the native Better Proposals API, this operation is `POST /quote/create` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

