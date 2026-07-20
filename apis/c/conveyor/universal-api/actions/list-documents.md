# Conveyor: List Documents

Retrieves documents from the Conveyor exchange.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-documents?${params}`, {
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
      "_embedded": {
        "documents": [
          {
            "access_level": "string",
            "id": "string",
            "name": "Ava Chen",
            "updated_at": "2026-05-07T12:00:00.000Z"
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
| `_embedded` | object |  |
| `_embedded.documents` | array<object> |  |
| `_embedded.documents[].access_level` | string |  |
| `_embedded.documents[].id` | string |  |
| `_embedded.documents[].name` | string |  |
| `_embedded.documents[].updated_at` | date |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/exchange/documents` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

