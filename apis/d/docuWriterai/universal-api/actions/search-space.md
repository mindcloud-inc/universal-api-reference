# DocuWriter.ai: Search Space



```
GET https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/search-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/search-space?connectionId=$CONNECTION_ID&query=string&space=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "space": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/search-space?${params}`, {
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
| `highlight` | boolean | no | Whether to wrap matched terms in mark tags. Default: `true`. |
| `page` | number | no | Page number for paginated results. Default: `1`. |
| `perPage` | number | no | Number of results per page. Default: `20`. |
| `query` | string | yes | Search keyword or phrase. |
| `space` | string | yes | Space ID or slug to search within. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "query": "string",
      "results": [
        {}
      ],
      "space": {},
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `query` | string | Query string echoed by DocuWriter. |
| `results` | array<object> | Matched search results. |
| `space` | object | Space metadata for the searched space. |
| `total` | number | Total number of matching results. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `POST /api/spaces/{{space}}/search` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-space.md) for the provider-specific parameters and requirements.

