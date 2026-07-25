# Outlign: List Projects

Retrieves accessible project records from Outlign.

```
GET https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-projects?${params}`, {
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
| `perPage` | number | no | Number of results per page (max 1000) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "client": {},
          "clientProjectType": "string",
          "company": {},
          "createdAt": "string",
          "description": "string",
          "id": 1,
          "internalProjectType": "string",
          "isClient": true,
          "isInternal": true,
          "title": "string",
          "updatedAt": "string"
        }
      ],
      "links": {
        "first": "https://example.com",
        "last": {},
        "next": "https://example.com",
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
| `data[].client` | object |  |
| `data[].clientProjectType` | string |  |
| `data[].company` | object |  |
| `data[].createdAt` | string |  |
| `data[].description` | string |  |
| `data[].id` | number |  |
| `data[].internalProjectType` | string |  |
| `data[].isClient` | boolean |  |
| `data[].isInternal` | boolean |  |
| `data[].title` | string |  |
| `data[].updatedAt` | string |  |
| `links.first` | string |  |
| `links.last` | object |  |
| `links.next` | string |  |
| `links.prev` | object |  |
| `meta.currentPage` | number |  |
| `meta.currentPageUrl` | string |  |
| `meta.from` | number |  |
| `meta.path` | string |  |
| `meta.perPage` | number |  |
| `meta.to` | number |  |

## Native endpoint

Through the native Outlign API, this operation is `GET /projects` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

