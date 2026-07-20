# JustSift: Advanced People Search



```
GET https://connect.mindcloud.co/v1/universal/justSift/latest/actions/advanced-people-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustSift `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justSift/latest/actions/advanced-people-search?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justSift/latest/actions/advanced-people-search?${params}`, {
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
| `q` | string | no | Generic term searched across searchable Sift fields. |
| `page` | number | no | Page number to retrieve. Sift pages start at 1. Default: `1`. |
| `pageSize` | number | no | Number of people to return, from 0 to 100. Default: `10`. |
| `sortBy` | string | no | Sift field objectKey to sort by. |
| `sortDirection` | string | no | Sort direction, asc or desc. One of: `0`, `1`. Default: `asc`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | object | no | Advanced Sift PeopleFilters object using and, or, not, or field comparison clauses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "department": "string",
      "directoryId": "string",
      "directReportCount": 1,
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isTeamLeader": true,
      "lastName": "Chen",
      "pictureUrl": "https://example.com",
      "reportingPath": [
        "string"
      ],
      "teamLeaderId": "string",
      "title": "string",
      "totalReportCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `department` | string | Department. |
| `directoryId` | string | Directory identifier. |
| `directReportCount` | number | Number of direct reports. |
| `displayName` | string | Person display name. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `id` | string | Unique person identifier. |
| `isTeamLeader` | boolean | Whether the person has direct reports. |
| `lastName` | string | Last name. |
| `pictureUrl` | string | Profile picture URL. |
| `reportingPath` | array<string> | Hierarchy path of leader ids. |
| `teamLeaderId` | string | Direct leader person identifier. |
| `title` | string | Job title. |
| `totalReportCount` | number | Total direct and indirect reports. |

## Native endpoint

Through the native JustSift API, this operation is `POST /search/people` (base URL `https://api.justsift.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/advanced-people-search.md) for the provider-specific parameters and requirements.

