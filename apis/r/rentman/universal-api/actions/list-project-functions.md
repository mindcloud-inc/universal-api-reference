# Rentman: List Project Functions



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-functions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-functions?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-functions?${params}`, {
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
| `id` | number | yes | Numeric Rentman project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cost_rate": "string",
      "costs_variable": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "displayname": "Ava Chen",
      "duration": 1,
      "id": 1,
      "in_financial": true,
      "in_planning": true,
      "is_plannable": true,
      "ledger": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "price_rate": "string",
      "price_variable": 1,
      "project": "string",
      "subproject": "string",
      "taxclass": "string",
      "type": "string",
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `cost_rate` | string |  |
| `costs_variable` | number |  |
| `created` | date |  |
| `creator` | string |  |
| `displayname` | string |  |
| `duration` | number |  |
| `id` | number |  |
| `in_financial` | boolean |  |
| `in_planning` | boolean |  |
| `is_plannable` | boolean |  |
| `ledger` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `price_rate` | string |  |
| `price_variable` | number |  |
| `project` | string |  |
| `subproject` | string |  |
| `taxclass` | string |  |
| `type` | string |  |
| `updateHash` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /projects/:id/projectfunctions` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-functions.md) for the provider-specific parameters and requirements.

