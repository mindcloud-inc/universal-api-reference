# Productlane: List Companies

Retrieves companies from your Productlane workspace.

```
GET https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productlane/latest/actions/list-companies?${params}`, {
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
| `domain` | string | no | Filter companies by domain. |
| `name` | string | no | Filter companies by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoAdd": {},
      "Count": {
        "contacts": 1
      },
      "createdAt": "string",
      "domains": [
        "string"
      ],
      "externalIds": [
        "string"
      ],
      "hubspotId": {},
      "id": "string",
      "intercomId": {},
      "isDeleted": true,
      "linearCustomerId": {},
      "logoUrl": {},
      "meta": {},
      "name": "Ava Chen",
      "productboardId": {},
      "revenue": {},
      "size": {},
      "slugId": {},
      "statusColor": {},
      "statusId": {},
      "statusName": {},
      "tierId": {},
      "tierName": {},
      "updatedAt": "string",
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
| `autoAdd` | object |  |
| `Count.contacts` | number |  |
| `createdAt` | string |  |
| `domains[]` | string |  |
| `externalIds[]` | string |  |
| `hubspotId` | object |  |
| `id` | string |  |
| `intercomId` | object |  |
| `isDeleted` | boolean |  |
| `linearCustomerId` | object |  |
| `logoUrl` | object |  |
| `meta` | object |  |
| `name` | string |  |
| `productboardId` | object |  |
| `revenue` | object |  |
| `size` | object |  |
| `slugId` | object |  |
| `statusColor` | object |  |
| `statusId` | object |  |
| `statusName` | object |  |
| `tierId` | object |  |
| `tierName` | object |  |
| `updatedAt` | string |  |
| `version` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Productlane API, this operation is `GET /companies` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

