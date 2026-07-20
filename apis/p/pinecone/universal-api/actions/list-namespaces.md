# Pinecone: List Namespaces

Retrieves namespaces from a Pinecone index.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-namespaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-namespaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/list-namespaces?${params}`, {
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
| `prefix` | string | no | Only return namespaces that start with this prefix. Example: `prod-`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "namespaces": [
        {
          "name": "Ava Chen",
          "record_count": "Ava Chen"
        }
      ],
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `namespaces[].name` | string |  |
| `namespaces[].record_count` | string |  |
| `total_count` | number |  |

## Native endpoint

Through the native Pinecone API, this operation is `GET {{credentials.indexHost}}/namespaces` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-namespaces.md) for the provider-specific parameters and requirements.

