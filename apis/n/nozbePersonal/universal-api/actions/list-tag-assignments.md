# Nozbe Personal: List Tag Assignments

Retrieves accessible tag assignments from Nozbe Personal.

```
GET https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-tag-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-tag-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-tag-assignments?${params}`, {
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
| `taskId` | string | no | Return assignments for this task. Example: `L2TZ05o6wV41fjMe`. |
| `tagId` | string | no | Return assignments for this tag. Example: `L2TZ05o6wV41fjMe`. |
| `fields` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "tagId": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `tagId` | string |  |
| `taskId` | string |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `GET /tag_assignments` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tag-assignments.md) for the provider-specific parameters and requirements.

