# Autype: List Documents

Retrieves documents from Autype.

```
GET https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autype/latest/actions/list-documents?${params}`, {
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
| `projectId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": {},
          "id": "string",
          "projectId": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "limit": 1,
      "page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents[].createdAt` | date |  |
| `documents[].description` | object |  |
| `documents[].id` | string |  |
| `documents[].projectId` | string |  |
| `documents[].title` | string |  |
| `documents[].updatedAt` | date |  |
| `limit` | number |  |
| `page` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Autype API, this operation is `GET /documents` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

