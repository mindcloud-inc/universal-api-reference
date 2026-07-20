# 4HSE: List Projects

Retrieves projects from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-projects?${params}`, {
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
| `filter` | object | no | Project filters. |
| `filter.name` | string | no | Search a project by company name. |
| `filter.status` | string | no | Filter by lifecycle status. |
| `filter.projectType` | string | no | Filter by project type. |
| `history` | boolean | no | Include historized entries when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeNpeople": 1,
      "country": "string",
      "createdAt": "string",
      "customerId": "string",
      "deletedAt": "string",
      "description": "string",
      "icon": "string",
      "name": "Ava Chen",
      "npeople": 1,
      "partnerId": "string",
      "partnerName": "Ava Chen",
      "permission": "string",
      "planId": "string",
      "projectId": "string",
      "projectType": "string",
      "status": "string",
      "subscriptionId": "string",
      "subscriptionStatus": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeNpeople` | number | Number of active workers. |
| `country` | string | ISO 3166-1 alpha-2 country code. |
| `createdAt` | string | Creation date. |
| `customerId` | string | Customer identifier. |
| `deletedAt` | string | Scheduled deletion date. |
| `description` | string | Optional free-text description. |
| `icon` | string | URL of the project icon image. |
| `name` | string | The company name. |
| `npeople` | number | Number of active workers in this project. |
| `partnerId` | string | Partner identifier. |
| `partnerName` | string | Partner name. |
| `permission` | string | Permission level for the current user. |
| `planId` | string | Plan identifier. |
| `projectId` | string | Unique identifier of the project. |
| `projectType` | string | Type of the project. |
| `status` | string | Project lifecycle status. |
| `subscriptionId` | string | Subscription identifier. |
| `subscriptionStatus` | string | Subscription status. |
| `updatedAt` | string | Last modification date. |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/project/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

