# Linkbreakers: List Links

Retrieves a list of links from Linkbreakers.

```
GET https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-links?${params}`, {
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
| `search` | string | no | Filter links by name or shortlink search. |
| `tags[]` | array<string> | no | Filter links by tags; matches links containing any provided tag. |
| `directoryId` | string | no | Filter links by one directory ID. |
| `includeAllDirectories` | boolean | no | Ignore the directory filter and return links from all directories. |
| `sortBy` | string | no | Field used to sort links. |
| `sortDirection` | string | no | Sort direction for list ordering. |
| `include[]` | array<string> | no | Related link resources to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        {
          "createdAt": "https://example.com",
          "destination": "https://example.com",
          "directoryId": "https://example.com",
          "entrypoint": "https://example.com",
          "eventCount": 1,
          "id": "https://example.com",
          "metadata": {},
          "name": "https://example.com",
          "shortlink": "https://example.com",
          "updatedAt": "https://example.com",
          "workspaceId": "https://example.com"
        }
      ],
      "nextPageToken": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | array<object> | Page of shortened links. |
| `links[].createdAt` | string |  |
| `links[].destination` | string |  |
| `links[].directoryId` | string |  |
| `links[].entrypoint` | string |  |
| `links[].eventCount` | number |  |
| `links[].id` | string |  |
| `links[].metadata` | object |  |
| `links[].name` | string |  |
| `links[].shortlink` | string |  |
| `links[].updatedAt` | string |  |
| `links[].workspaceId` | string |  |
| `nextPageToken` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `GET /v1/links` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

