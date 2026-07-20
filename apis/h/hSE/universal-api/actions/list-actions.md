# 4HSE: List Actions

Retrieves actions from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-actions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-actions?${params}`, {
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
| `filter` | object | no | Action filters. |
| `filter.actionType` | string | no | Filter by preventive action type. One of: `0`, `1`, `2`, `3`, `4`. Example: `TRAINING`. |
| `filter.name` | string | no | Search an action by name. Example: `Safety`. |
| `filter.subtenantId` | string | no | Filter by office id. Example: `2fdc699f-e67a-46dc-81a6-b03bb029dd07`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter.actionId` | string | no | Find one action by id. Example: `c4d5e6f7-a8b9-0c1d-2e3f-4a5b6c7d8e9f`. |
| `filter.tenantId` | string | no | Filter by project id. Example: `global`. |
| `history` | boolean | no | Include historicized entries when true. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionId": "string",
      "actionType": "string",
      "code": "string",
      "description": "string",
      "name": "Ava Chen",
      "officeId": "string",
      "officeName": "Ava Chen",
      "permission": "string",
      "projectName": "Ava Chen",
      "status": "string",
      "tenantId": "string",
      "validity": 1,
      "validityUnit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | string | 4HSE action identifier |
| `actionType` | string | Action type |
| `code` | string | Action code |
| `description` | string | Action description |
| `name` | string | Action name |
| `officeId` | string | Office identifier |
| `officeName` | string | Office name |
| `permission` | string | Permission level |
| `projectName` | string | Project name |
| `status` | string | Action status |
| `tenantId` | string | Project identifier |
| `validity` | number | Validity interval value |
| `validityUnit` | string | Validity interval unit |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/action/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-actions.md) for the provider-specific parameters and requirements.

