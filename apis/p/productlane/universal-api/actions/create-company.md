# Productlane: Create Company

Creates a new company in Productlane.

```
POST https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `domains[]` | array<string> | no |  |
| `autoAdd` | boolean | no |  |
| `externalIds[]` | array<string> | no |  |
| `size` | number | no |  |
| `revenue` | number | no |  |
| `tierId` | string | no |  |
| `tierName` | string | no |  |
| `statusId` | string | no |  |
| `statusName` | string | no |  |
| `statusColor` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoAdd": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domains": [
        "string"
      ],
      "externalIds": [
        "string"
      ],
      "hubspotId": "string",
      "id": "string",
      "intercomId": "string",
      "isDeleted": true,
      "linearCustomerId": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "productboardId": "string",
      "revenue": 1,
      "size": 1,
      "slugId": "string",
      "statusColor": "string",
      "statusId": "string",
      "statusName": "Ava Chen",
      "tierId": "string",
      "tierName": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoAdd` | boolean |  |
| `createdAt` | date |  |
| `domains` | array<string> |  |
| `externalIds` | array<string> |  |
| `hubspotId` | string |  |
| `id` | string |  |
| `intercomId` | string |  |
| `isDeleted` | boolean |  |
| `linearCustomerId` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `productboardId` | string |  |
| `revenue` | number |  |
| `size` | number |  |
| `slugId` | string |  |
| `statusColor` | string |  |
| `statusId` | string |  |
| `statusName` | string |  |
| `tierId` | string |  |
| `tierName` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Productlane API, this operation is `POST /companies` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

