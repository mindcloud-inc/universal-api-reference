# Linkbreakers: List Visitors

Retrieves a list of visitors from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-visitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-visitors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-visitors?${params}`, {
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
| `email` | string | no | Exact-match email filter. |
| `search` | string | no | Fuzzy search across visitor fields. |
| `include[]` | array<string> | no | Relationships to include in the response. |
| `linkId` | string | no | Filter visitors by link ID. |
| `responseFormat` | string | no | Desired response format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "csv": {
        "contentType": "string",
        "csvData": "string"
      },
      "json": {
        "hasMore": true,
        "nextPageToken": "string",
        "totalCount": 1,
        "visitors": [
          {
            "attributes": {},
            "createdAt": "string",
            "devices": [
              {}
            ],
            "email": "ava@example.com",
            "events": [
              {}
            ],
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": [
              {}
            ],
            "phone": "string",
            "updatedAt": "string",
            "workspaceId": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `csv` | object | CSV export payload when CSV format is requested. |
| `csv.contentType` | string |  |
| `csv.csvData` | string |  |
| `json` | object | Structured visitors response. |
| `json.hasMore` | boolean |  |
| `json.nextPageToken` | string |  |
| `json.totalCount` | number |  |
| `json.visitors` | array<object> |  |
| `json.visitors[].attributes` | object |  |
| `json.visitors[].createdAt` | string |  |
| `json.visitors[].devices` | array<object> |  |
| `json.visitors[].email` | string |  |
| `json.visitors[].events` | array<object> |  |
| `json.visitors[].firstName` | string |  |
| `json.visitors[].id` | string |  |
| `json.visitors[].lastName` | string |  |
| `json.visitors[].links` | array<object> |  |
| `json.visitors[].phone` | string |  |
| `json.visitors[].updatedAt` | string |  |
| `json.visitors[].workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/visitors` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-visitors.md) for the provider-specific parameters and requirements.

