# Billingo: List Document Blocks

Retrieves document blocks from your Billingo account.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-document-blocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-document-blocks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/list-document-blocks?${params}`, {
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
      "custom_field1": "string",
      "custom_field2": "string",
      "id": 1,
      "name": "Ava Chen",
      "prefix": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_field1` | string |  |
| `custom_field2` | string |  |
| `id` | number |  |
| `name` | string |  |
| `prefix` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /document-blocks` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-document-blocks.md) for the provider-specific parameters and requirements.

