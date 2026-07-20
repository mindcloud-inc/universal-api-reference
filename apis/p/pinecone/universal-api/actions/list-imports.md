# Pinecone: List Imports

Retrieves imports from a Pinecone index.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-imports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-imports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-imports?${params}`, {
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
          "createdAt": "2026-05-07T12:00:00.000Z",
          "error": "string",
          "finishedAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "percentComplete": 1,
          "recordsImported": 1,
          "status": "string",
          "uri": "string"
        }
      ],
      "pagination": {
        "next": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdAt` | date |  |
| `data[].error` | string |  |
| `data[].finishedAt` | date |  |
| `data[].id` | string |  |
| `data[].percentComplete` | number |  |
| `data[].recordsImported` | number |  |
| `data[].status` | string |  |
| `data[].uri` | string |  |
| `pagination.next` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET {{credentials.indexHost}}/bulk/imports` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-imports.md) for the provider-specific parameters and requirements.

