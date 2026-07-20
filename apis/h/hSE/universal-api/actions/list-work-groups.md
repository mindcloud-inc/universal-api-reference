# 4HSE: List Work Groups

Retrieves work groups from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-work-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-work-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-work-groups?${params}`, {
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
| `filter` | object | no | Search filters. |
| `filter.officeId` | string | no | Filter by office ID. |
| `filter.workGroupType` | string | no | Filter by work group type. |
| `filter.name` | string | no | Filter by name. |
| `filter.projectId` | string | no | Filter by project ID. |
| `history` | boolean | no | Include historicized work groups. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "description": "string",
      "name": "Ava Chen",
      "officeId": "string",
      "officeName": "Ava Chen",
      "ownedActive": true,
      "parentActive": true,
      "permission": "string",
      "projectId": "string",
      "projectName": "Ava Chen",
      "projectType": "string",
      "workGroupId": "string",
      "workGroupType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `description` | string |  |
| `name` | string |  |
| `officeId` | string |  |
| `officeName` | string |  |
| `ownedActive` | boolean |  |
| `parentActive` | boolean |  |
| `permission` | string |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `projectType` | string |  |
| `workGroupId` | string |  |
| `workGroupType` | string |  |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/work-group/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-groups.md) for the provider-specific parameters and requirements.

