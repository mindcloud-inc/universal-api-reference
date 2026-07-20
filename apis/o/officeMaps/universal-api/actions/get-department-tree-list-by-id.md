# OfficeMaps: Get Department Tree List By Id

Retrieves a department tree from OfficeMaps by department ID.

```
GET https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-tree-list-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-tree-list-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-tree-list-by-id?${params}`, {
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
| `id` | string | yes | Department UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "by": "string",
      "code": "string",
      "departmentHierachy": "string",
      "departmentId": "string",
      "description": "string",
      "fileDateString": "string",
      "fileRecordId": "string",
      "instanceId": "string",
      "isHidden": true,
      "isVisible": true,
      "name": "Ava Chen",
      "parentDepartmentId": "string",
      "searchTags": "string",
      "subDepartments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `by` | string | Department owner or source value when present. |
| `code` | string | Department code when present. |
| `departmentHierachy` | string | Department hierarchy path. |
| `departmentId` | string | Department UUID. |
| `description` | string | Department description. |
| `fileDateString` | string | Associated file date string when present. |
| `fileRecordId` | string | Associated file UUID when present. |
| `instanceId` | string | OfficeMaps instance UUID. |
| `isHidden` | boolean | Whether the department is hidden. |
| `isVisible` | boolean | Whether the department is visible. |
| `name` | string | Department name. |
| `parentDepartmentId` | string | Parent department UUID when present. |
| `searchTags` | string | Department search tags. |
| `subDepartments` | array<object> | Nested sub-departments. |

## Native endpoint

Through the native OfficeMaps API, this operation is `GET /v1/department/treelist/:id` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-department-tree-list-by-id.md) for the provider-specific parameters and requirements.

