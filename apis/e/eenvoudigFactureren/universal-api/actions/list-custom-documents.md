# EenvoudigFactureren: List Custom Documents

Retrieves custom documents from EenvoudigFactureren.

```
GET https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-custom-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-custom-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-custom-documents?${params}`, {
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
      "client_name": "Ava Chen",
      "customdocument_id": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "status": "string",
      "total": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_name` | string |  |
| `customdocument_id` | number |  |
| `date` | date |  |
| `number` | string |  |
| `status` | string |  |
| `total` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `GET /customdocuments` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-documents.md) for the provider-specific parameters and requirements.

