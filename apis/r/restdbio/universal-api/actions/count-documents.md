# Restdb.io: Count Documents

Retrieves document counts from a Restdb.io collection.

```
GET https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/count-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restdb.io `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/count-documents?connectionId=$CONNECTION_ID&collection=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collection": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/count-documents?${params}`, {
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
| `collection` | string | yes | Collection name in the target Restdb.io database. |
| `q` | string | no | JSON query string to count matching documents only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "totals": {
        "count": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `totals.count` | number |  |

## Native endpoint

Through the native Restdb.io API, this operation is `GET /rest/:collection` (base URL `https://mindcloudstage0-7934.restdb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-documents.md) for the provider-specific parameters and requirements.

