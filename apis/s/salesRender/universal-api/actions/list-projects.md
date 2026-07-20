# SalesRender: List Projects

Retrieves projects from SalesRender.

```
GET https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-projects?connectionId=$CONNECTION_ID&query=query%20%7B%20projectsFetcher%20%7B%20projects%20%7B%20id%20name%20archived%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { projectsFetcher { projects { id name archived } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-projects?${params}`, {
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
| `query` | string | yes | GraphQL query to execute against SalesRender. Default: `query {\n  projectsFetcher {\n    projects {\n      id\n      name\n      archived\n    }\n  }\n}`. Example: `query { projectsFetcher { projects { id name archived } } }`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | Optional GraphQL variables object. Default: `{}`. Example: `Optional JSON variables string`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "projectsFetcher": {
          "projects": [
            {
              "archived": true,
              "id": "string",
              "name": "Ava Chen"
            }
          ]
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
| `data.projectsFetcher.projects[].archived` | boolean | Whether the project is archived. |
| `data.projectsFetcher.projects[].id` | string | Project ID. |
| `data.projectsFetcher.projects[].name` | string | Project name. |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

