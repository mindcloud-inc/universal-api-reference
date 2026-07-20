# OfficeMaps: Get Departments

Retrieves departments from OfficeMaps with membership data.

```
GET https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-departments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-departments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "administrators": [
        "string"
      ],
      "departmentId": "string",
      "isHidden": true,
      "managers": [
        "string"
      ],
      "members": [
        "string"
      ],
      "name": "Ava Chen",
      "parentDepartmentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrators` | array<string> | Department administrator person IDs. |
| `departmentId` | string | Department UUID. |
| `isHidden` | boolean | Whether the department is hidden. |
| `managers` | array<string> | Department manager person IDs. |
| `members` | array<string> | Department member person IDs. |
| `name` | string | Department name. |
| `parentDepartmentId` | string | Parent department UUID when present. |

## Native endpoint

Through the native OfficeMaps API, this operation is `GET /v1/department` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-departments.md) for the provider-specific parameters and requirements.

