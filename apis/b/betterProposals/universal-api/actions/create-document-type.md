# Better Proposals: Create Document Type

Creates a document type in Better Proposals.

```
POST https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "typeName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-document-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "typeName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `typeName` | string | yes | Document type name. |
| `typeColour` | string | no | Colour for the new document type. Default is #01A3EF. Default: `#01A3EF`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "categoryIcon": {},
      "createdBy": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateDeleted": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "deleted": "string",
      "deletedBy": {},
      "displayOrder": {},
      "editedBy": {},
      "id": "string",
      "typeColour": "string",
      "typeIcon": {},
      "typeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `categoryIcon` | object |  |
| `createdBy` | string |  |
| `dateCreated` | date |  |
| `dateDeleted` | date |  |
| `dateEdited` | date |  |
| `deleted` | string |  |
| `deletedBy` | object |  |
| `displayOrder` | object |  |
| `editedBy` | object |  |
| `id` | string |  |
| `typeColour` | string |  |
| `typeIcon` | object |  |
| `typeName` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `POST /doctype/create` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-type.md) for the provider-specific parameters and requirements.

