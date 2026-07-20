# Leiga: Get Project by Project Key

Retrieves a project from Leiga by project key.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-project-by-project-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-project-by-project-key?connectionId=$CONNECTION_ID&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/get-project-by-project-key?${params}`, {
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
| `projectKey` | string | yes | Project Key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": 1,
      "avatar": 1,
      "createBy": 1,
      "createTime": 1,
      "description": "string",
      "id": 1,
      "leader": "string",
      "leaderId": 1,
      "projectCategory": 1,
      "projectKey": "string",
      "projectName": "Ava Chen",
      "status": 1,
      "updateTime": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | number | Archived flag. |
| `avatar` | number | Project avatar ID. |
| `createBy` | number | Project creator ID. |
| `createTime` | number | Creation timestamp. |
| `description` | string | Project description. |
| `id` | number | Project ID. |
| `leader` | string | Project leader name. |
| `leaderId` | number | Project leader ID. |
| `projectCategory` | number | Project category ID. |
| `projectKey` | string | Project key. |
| `projectName` | string | Project name. |
| `status` | number | Project status. |
| `updateTime` | number | Last update timestamp. |
| `url` | string | Project URL. |

## Native endpoint

Through the native Leiga API, this operation is `GET /project/get-by-project-key` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-by-project-key.md) for the provider-specific parameters and requirements.

