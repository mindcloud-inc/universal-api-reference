# Pipedrive: Get Organizations

Retrieves organizations from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-organizations?${params}`, {
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
| `limit` | number | no | Maximum number of organizations to return. |
| `cursor` | string | no | Pagination cursor from a previous response. |
| `sortBy` | string | no | Field used for sorting results. |
| `sortDirection` | string | no | Sort direction: asc or desc. |
| `ownerId` | number | no | Filter organizations by owner user ID. |
| `filterId` | number | no | Filter organizations by saved filter ID. |
| `firstChar` | string | no | Filter organizations by first character of name. |
| `ids` | string | no | Comma-separated list of organization IDs. |
| `includeFields` | string | no | Comma-separated additional fields to include. |
| `customFields` | string | no | Comma-separated custom field keys to include. |
| `updatedSince` | string | no | Return organizations updated after this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "addTime": "string",
      "annualRevenue": {},
      "customFields": {},
      "employeeCount": {},
      "id": 1,
      "industry": {},
      "isDeleted": true,
      "linkedin": {},
      "name": "Ava Chen",
      "ownerId": 1,
      "updateTime": "string",
      "visibleTo": 1,
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `addTime` | string |  |
| `annualRevenue` | object |  |
| `customFields` | object |  |
| `employeeCount` | object |  |
| `id` | number |  |
| `industry` | object |  |
| `isDeleted` | boolean |  |
| `linkedin` | object |  |
| `name` | string |  |
| `ownerId` | number |  |
| `updateTime` | string |  |
| `visibleTo` | number |  |
| `website` | object |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/organizations` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-organizations.md) for the provider-specific parameters and requirements.

