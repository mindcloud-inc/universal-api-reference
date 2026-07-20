# Leiga: List Project Members

Retrieves project members from Leiga with pagination.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-members?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-members?${params}`, {
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
| `projectId` | number | yes | Project ID |
| `keyword` | string | no | Keyword for search |
| `pageNumber` | number | no | Page Number |
| `pageSize` | number | no | Page Size |

## Response

```json
{
  "success": true,
  "data": [
    {
      "departmentVOList": [
        {}
      ],
      "head": "string",
      "orgEmail": "ava@example.com",
      "roleVOList": [
        {}
      ],
      "userId": 1,
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `departmentVOList` | array<object> | Department entries. |
| `head` | string | Member avatar URL. |
| `orgEmail` | string | Member email address. |
| `roleVOList` | array<object> | Project role entries. |
| `userId` | number | Member user ID. |
| `userName` | string | Member name. |

## Native endpoint

Through the native Leiga API, this operation is `GET /user/project-user-page` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-members.md) for the provider-specific parameters and requirements.

