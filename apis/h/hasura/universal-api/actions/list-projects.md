# Hasura: List Projects

Retrieves projects from Hasura Cloud.

```
GET https://connect.mindcloud.co/v1/universal/hasura/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hasura `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasura/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasura/latest/actions/list-projects?${params}`, {
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
      "data": {
        "projects": {
          "endpoint": "string",
          "id": "string",
          "name": "Ava Chen",
          "tenant": {
            "id": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.projects` | array<object> | Hasura Cloud projects. |
| `data.projects.endpoint` | string | Project GraphQL endpoint. |
| `data.projects.id` | string | Project ID. |
| `data.projects.name` | string | Project name. |
| `data.projects.tenant.id` | string | Tenant ID associated with the project. |

## Native endpoint

Through the native Hasura API, this operation is `POST /v1/graphql` (base URL `https://data.pro.hasura.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

