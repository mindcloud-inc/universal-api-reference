# Better Proposals: Create Company

Creates a company in Better Proposals.

```
POST https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyName` | string | yes | Company name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "companyCRMID": {},
      "companyName": "Ava Chen",
      "createdBy": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "deleted": "string",
      "deletedBy": {},
      "demoCompany": "string",
      "editedBy": {},
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `companyCRMID` | object |  |
| `companyName` | string |  |
| `createdBy` | string |  |
| `dateCreated` | date |  |
| `dateEdited` | date |  |
| `deleted` | string |  |
| `deletedBy` | object |  |
| `demoCompany` | string |  |
| `editedBy` | object |  |
| `id` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `POST /company/create` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

