# Zoho WorkDrive: Search across Team

Finds files and folders in Zoho WorkDrive across a team.

```
GET https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/search-across-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho WorkDrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/search-across-team?connectionId=$CONNECTION_ID&limit=25&offset=0&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWorkDrive/latest/actions/search-across-team?${params}`, {
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
| `teamId` | string | yes | The WorkDrive team ID. |
| `searchQuery` | string | no | Search text to match across names or content. |
| `filterParentId` | string | no | Restrict the search to a specific parent folder. |
| `filterType` | string | no | Filter the results by resource type. |
| `filterDate` | string | no | Use a predefined date filter range. |
| `filterFromDate` | string | no | Start date for the filter range. |
| `filterToDate` | string | no | End date for the filter range. |
| `filterStatus` | string | no | Filter by the WorkDrive file status. |
| `filterCreator` | string | no | Filter by the creator of the resource. |
| `limit` | string | no | Maximum number of records to return. |
| `offset` | string | no | Number of records to skip before returning results. |
| `sort` | string | no | Sort expression for the returned resources. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Provider resource attributes. |
| `id` | string | Resource ID. |
| `links` | object | Provider self and related links. |
| `relationships` | object | Provider relationship links. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Zoho WorkDrive API, this operation is `GET /api/v1/teams/:teamId/records` (base URL `{{credentials.accessTokenRequest.api_domain}}/workdrive`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-across-team.md) for the provider-specific parameters and requirements.

