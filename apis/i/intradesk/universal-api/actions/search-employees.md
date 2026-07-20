# Intradesk: Search Employees

Finds employees in Intradesk by search text.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/search-employees?${params}`, {
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
| `searchString` | string | no | Employee hint search text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `top` | number | no | Maximum number of employee hints to return. |
| `excludedids[]` | array<number> | no | Employee IDs to exclude from hint results. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "fullName": "Ava Chen",
      "id": 1,
      "isArchived": true,
      "level": 1,
      "name": "Ava Chen",
      "namePath": "Ava Chen",
      "path": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `level` | number |  |
| `name` | string |  |
| `namePath` | string |  |
| `path` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /settings/api/v1/Employees/SearchHints` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-employees.md) for the provider-specific parameters and requirements.

