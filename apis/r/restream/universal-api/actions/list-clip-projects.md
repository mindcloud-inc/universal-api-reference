# Restream: List Clip Projects

Retrieves clip projects from Restream.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/list-clip-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/list-clip-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/list-clip-projects?${params}`, {
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
| `cursor` | string | no | Cursor from the previous response. |
| `limit` | number | no | Maximum number of projects to return. |
| `sortBy` | string | no | Sort order for results: CreatedAt or LastActivity. Example: `CreatedAt or LastActivity`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "projects": [
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
| `pagination` | object |  |
| `projects` | array<object> |  |

## Native endpoint

Through the native Restream API, this operation is `GET /user/clips/projects` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clip-projects.md) for the provider-specific parameters and requirements.

