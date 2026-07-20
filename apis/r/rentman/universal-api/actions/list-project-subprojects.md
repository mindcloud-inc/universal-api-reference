# Rentman: List Project Subprojects



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-subprojects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-subprojects?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-subprojects?${params}`, {
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
| `id` | number | yes | Numeric ID of the parent project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asset_location_from": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "displayname": "Ava Chen",
      "fixed_price": true,
      "id": 1,
      "in_financial": true,
      "in_planning": true,
      "insurance_rate": 1,
      "is_template": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "order": 1,
      "project": "string",
      "status": "string",
      "updateHash": "string",
      "usageperiod_end": "2026-05-07T12:00:00.000Z",
      "usageperiod_start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset_location_from` | string |  |
| `created` | date |  |
| `creator` | string |  |
| `displayname` | string |  |
| `fixed_price` | boolean |  |
| `id` | number |  |
| `in_financial` | boolean |  |
| `in_planning` | boolean |  |
| `insurance_rate` | number |  |
| `is_template` | boolean |  |
| `modified` | date |  |
| `name` | string |  |
| `order` | number |  |
| `project` | string |  |
| `status` | string |  |
| `updateHash` | string |  |
| `usageperiod_end` | date |  |
| `usageperiod_start` | date |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /projects/:id/subprojects` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-subprojects.md) for the provider-specific parameters and requirements.

