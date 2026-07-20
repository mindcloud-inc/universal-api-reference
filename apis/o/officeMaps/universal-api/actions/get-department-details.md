# OfficeMaps: Get Department Details

Retrieves department details from OfficeMaps.

```
GET https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-details?connectionId=$CONNECTION_ID&departmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "departmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-details?${params}`, {
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
| `departmentId` | string | yes | The OfficeMaps department UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "departmentAdministrators": [
        "string"
      ],
      "departmentId": "string",
      "departmentManagers": [
        "string"
      ],
      "departmentMembers": [
        "string"
      ],
      "description": "string",
      "isHidden": true,
      "isVisible": true,
      "name": "Ava Chen",
      "parentDepartmentId": "string",
      "searchTags": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departmentAdministrators` | array<string> | Administrator person IDs. |
| `departmentId` | string | Department UUID. |
| `departmentManagers` | array<string> | Manager person IDs. |
| `departmentMembers` | array<string> | Member person IDs. |
| `description` | string | Department description. |
| `isHidden` | boolean | Whether the department is hidden. |
| `isVisible` | boolean | Whether the department is visible. |
| `name` | string | Department name. |
| `parentDepartmentId` | string | Parent department UUID when present. |
| `searchTags` | string | Search tags. |

## Native endpoint

Through the native OfficeMaps API, this operation is `GET /v1/department/:departmentId` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-department-details.md) for the provider-specific parameters and requirements.

