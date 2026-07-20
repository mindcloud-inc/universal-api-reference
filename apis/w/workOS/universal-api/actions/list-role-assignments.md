# WorkOS: List role assignments

Retrieves role assignments from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/list-role-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/list-role-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0&organization_membership_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organization_membership_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/list-role-assignments?${params}`, {
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
| `organization_membership_id` | string | yes | The ID of the organization membership. |
| `before` | string | no | An object ID that defines your place in the list. When the ID is not present, you are at the end of the list. For example, if you make a list request and receive 100 objects, ending with `"obj_123"`, your subsequent call can include `before="obj_123"` to fetch a new batch of objects before `"obj_123"`. |
| `after` | string | no | An object ID that defines your place in the list. When the ID is not present, you are at the end of the list. For example, if you make a list request and receive 100 objects, ending with `"obj_123"`, your subsequent call can include `after="obj_123"` to fetch a new batch of objects after `"obj_123"`. |
| `limit` | number | no | Upper limit on the number of objects to return, between `1` and `100`. |
| `order` | string | no | Order the results by the creation time. Supported values are `"asc"` (ascending), `"desc"` (descending), and `"normal"` (descending with reversed cursor semantics where `before` fetches older records and `after` fetches newer records). Defaults to descending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "id": "string",
      "list_metadata": {},
      "message": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | The list of records for the current page. |
| `id` | string | WorkOS response field id. |
| `list_metadata` | object | Pagination cursors for navigating between pages of results. |
| `message` | string | WorkOS response field message. |
| `object` | string | Indicates this is a list response. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /authorization/organization_memberships/{organization_membership_id}/role_assignments` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-role-assignments.md) for the provider-specific parameters and requirements.

