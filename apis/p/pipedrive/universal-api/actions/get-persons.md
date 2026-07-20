# Pipedrive: Get Persons

Retrieves person records from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-persons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-persons?${params}`, {
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
| `limit` | number | no | Maximum number of persons to return. |
| `cursor` | string | no | Pagination cursor from a previous response. |
| `sortBy` | string | no | Field used for sorting results. |
| `sortDirection` | string | no | Sort direction: asc or desc. |
| `ownerId` | number | no | Filter persons by owner user ID. |
| `filterId` | number | no | Filter persons by saved filter ID. |
| `firstChar` | string | no | Filter persons by the first character of name. |
| `ids` | string | no | Comma-separated list of person IDs. |
| `includeFields` | string | no | Comma-separated additional fields to include. |
| `customFields` | string | no | Comma-separated custom field keys to include. |
| `updatedSince` | string | no | Return persons updated after this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "customFields": {},
      "firstName": "Ava",
      "id": 1,
      "isDeleted": true,
      "lastName": "Chen",
      "name": "Ava Chen",
      "orgId": 1,
      "ownerId": 1,
      "pictureId": {},
      "updateTime": "string",
      "visibleTo": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addTime` | string |  |
| `customFields` | object |  |
| `firstName` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `lastName` | string |  |
| `name` | string |  |
| `orgId` | number |  |
| `ownerId` | number |  |
| `pictureId` | object |  |
| `updateTime` | string |  |
| `visibleTo` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/persons` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-persons.md) for the provider-specific parameters and requirements.

