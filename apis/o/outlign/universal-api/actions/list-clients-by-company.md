# Outlign: List Clients By Company

Retrieves client records from Outlign by company.

```
GET https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-clients-by-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlign `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-clients-by-company?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/list-clients-by-company?${params}`, {
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
| `companyId` | number | yes | Filter clients by company ID |
| `perPage` | number | no | Number of results per page (max 1000) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "company": {
            "id": 1,
            "title": "string"
          },
          "createdAt": "string",
          "id": 1,
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
| `data[].company.id` | number |  |
| `data[].company.title` | string |  |
| `data[].createdAt` | string |  |
| `data[].id` | number |  |
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

Through the native Outlign API, this operation is `GET /clients` (base URL `https://go.outlign.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients-by-company.md) for the provider-specific parameters and requirements.

