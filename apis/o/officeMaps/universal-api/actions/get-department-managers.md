# OfficeMaps: Get Department Managers

Retrieves managers in an OfficeMaps department.

```
GET https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-managers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-managers?connectionId=$CONNECTION_ID&departmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "departmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/get-department-managers?${params}`, {
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
| `departmentId` | string | yes | Department UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "page": 1,
      "pageSize": 1,
      "skip": 1,
      "sort": "string",
      "top": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Department managers. |
| `page` | number | Current page when provided. |
| `pageSize` | number | Page size when provided. |
| `skip` | number | Skipped record count when provided. |
| `sort` | string | Applied sort expression. |
| `top` | number | Top record count when provided. |
| `total` | number | Total matching people. |

## Native endpoint

Through the native OfficeMaps API, this operation is `GET /v1/department/:departmentId/managers` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-department-managers.md) for the provider-specific parameters and requirements.

