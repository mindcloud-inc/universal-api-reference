# Outlign: List Non-Template Tasks

Retrieves non-template task records from Outlign.

```
GET https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-non-template-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-non-template-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-non-template-tasks?${params}`, {
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
      "data": [
        {
          "assignees": [
            {
              "id": 1,
              "name": "Ava Chen"
            }
          ],
          "client": {
            "id": 1,
            "title": "string"
          },
          "company": {
            "id": 1,
            "title": "string"
          },
          "completed": true,
          "createdAt": "string",
          "dueDate": "string",
          "id": 1,
          "phase": {
            "id": 1,
            "isInternal": true,
            "title": "string"
          },
          "project": {
            "id": 1,
            "title": "string"
          },
          "published": true,
          "title": "string",
          "updatedAt": "string"
        }
      ],
      "links": {
        "first": "https://example.com",
        "last": {},
        "next": {},
        "prev": {}
      },
      "meta": {
        "currentPage": 1,
        "currentPageUrl": "https://example.com",
        "from": 1,
        "path": "string",
        "perPage": 1,
        "to": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].assignees[].id` | number |  |
| `data[].assignees[].name` | string |  |
| `data[].client.id` | number |  |
| `data[].client.title` | string |  |
| `data[].company.id` | number |  |
| `data[].company.title` | string |  |
| `data[].completed` | boolean |  |
| `data[].createdAt` | string |  |
| `data[].dueDate` | string |  |
| `data[].id` | number |  |
| `data[].phase.id` | number |  |
| `data[].phase.isInternal` | boolean |  |
| `data[].phase.title` | string |  |
| `data[].project.id` | number |  |
| `data[].project.title` | string |  |
| `data[].published` | boolean |  |
| `data[].title` | string |  |
| `data[].updatedAt` | string |  |
| `links.first` | string |  |
| `links.last` | object |  |
| `links.next` | object |  |
| `links.prev` | object |  |
| `meta.currentPage` | number |  |
| `meta.currentPageUrl` | string |  |
| `meta.from` | number |  |
| `meta.path` | string |  |
| `meta.perPage` | number |  |
| `meta.to` | number |  |

## Native endpoint

Through the native Outlign API, this operation is `GET /steps` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-non-template-tasks.md) for the provider-specific parameters and requirements.

